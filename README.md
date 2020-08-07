# onepluslogin
simpletest
mport java.util.List;
import java.util.concurrent.TimeUnit;
import org.openqa.selenium.By;
import org.openqa.selenium.WebDriver;
import org.openqa.selenium.WebElement;
import org.openqa.selenium.chrome.ChromeDriver;
import org.openqa.selenium.support.ui.ExpectedConditions;
import org.openqa.selenium.support.ui.Select;
import org.openqa.selenium.support.ui.WebDriverWait;

public class testcase1 {
	
	

	private static final By By = null;

	public static void main(String[] args) {
		
		System.setProperty("webdriver.chrome.driver", "C://chromedriver.exe");
		WebDriver driver = new ChromeDriver();
		driver.manage().window().maximize();
	
		
		driver.manage().deleteAllCookies();

		
		driver.manage().timeouts().pageLoadTimeout(40, TimeUnit.SECONDS);
		driver.manage().timeouts().implicitlyWait(30, TimeUnit.SECONDS);
	
		
		driver.get("https://account.oneplus.in/signin?callback=https%3A%2F%2Fwww.oneplus.in%2F&app=10&client=1&state=&cc=in&ts=1596781903977&sign=9a969f44045b43b2acc2a7574ca88bee&from=null");
		driver.findElement(By.xpath("//input[@name='input-email']")).sendKeys("9789857892");
		driver.findElement(By.xpath("//input[@name='login-otp']")).sendKeys("111111");

		WebElement click = driver.findElement(By.xpath("//*[@class='submit-btn full-width one-button btn-red frozen']"));
		click = driver.findElement(By.xpath("//*[@class='switch-login-btn one-button btn-black full-width one-button btn-red frozen']"));
		click.click();
		driver.findElement(By.xpath("//input[@name='input-email']")).sendKeys("kevinkarthi123@gmail.com");
		driver.findElement(By.xpath("//input[@name='input-password']")).sendKeys("123456789");
		click = driver.findElement(By.xpath("//*[@class='submit-btn full-width one-button btn-red frozen']"));
		click.click();
	}

}
