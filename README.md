# abcdpackage Action;

import org.openqa.selenium.By;
import org.openqa.selenium.WebDriver;
import org.openqa.selenium.WebElement;
import org.openqa.selenium.chrome.ChromeDriver;
import org.openqa.selenium.interactions.Actions;

public class Draganddrop {
	
	public static void main(String[] args) throws InterruptedException {
		
		System.setProperty("webdriver.chrome.driver", "C:\\Users\\SHREE\\Pictures\\chromedriver.exe");
		
		WebDriver driver = new ChromeDriver();
		
		driver.get("http://demo.automationtesting.in/Static.html");
		driver.manage().window().maximize();
		
		WebElement src = driver.findElement(By.xpath("//*[@id=\'mongo\']"));
		WebElement dest = driver.findElement(By.xpath("//*[@id=\"droparea\"]"));
		
		Actions act=new Actions(driver);
		Thread.sleep(2000);
		act.dragAndDrop(src, dest).perform();
		
	}
