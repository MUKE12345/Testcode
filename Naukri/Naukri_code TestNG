package Naukri;

import java.io.File;
import java.io.IOException;

import org.openqa.selenium.By;
import org.openqa.selenium.OutputType;
import org.openqa.selenium.TakesScreenshot;
import org.openqa.selenium.WebDriver;
import org.openqa.selenium.WebElement;
import org.openqa.selenium.chrome.ChromeDriver;
import org.openqa.selenium.io.FileHandler;
import org.openqa.selenium.support.ui.Select;
import org.testng.annotations.BeforeSuite;
import org.testng.annotations.Test;
import io.github.bonigarcia.wdm.WebDriverManager;
import org.testng.annotations.AfterSuite;


public class Naukri_com {

	
		
		WebDriver driver;
		@BeforeSuite
		public void Naukri() {
		WebDriverManager.chromedriver().setup();
		driver = new ChromeDriver();
	        
	  	//URL address
	  	driver.get("https://www.naukri.com/");
	  	driver.manage().window().maximize();
		}
		
		@Test(priority=1)
  	    //Click login
  		public void test1() throws InterruptedException {
  		WebElement Login =  driver.findElement(By.id("login_Layer"));
  		Login.click();
  		Thread.sleep(2000);
  		}

		@Test(priority=2)
  	    //Enter Username
  		public void test2() throws InterruptedException {
  		WebElement username =  driver.findElement(By.xpath("(//input[@type='text'])[1]"));
  		username.sendKeys("demo@gmail.com");
  		Thread.sleep(2000);
  		}
		
		@Test(priority=3)
  	    //Enter User password
  		public void test3() throws InterruptedException {
  		WebElement userpassword =  driver.findElement(By.xpath("(//input[@autocomplete='off'])[1]"));
  		userpassword.sendKeys("Abcdefg@123");
  		Thread.sleep(2000);
  		}
	
		@Test(priority=4)
  	    //Click login Button
  		public void test4() throws InterruptedException {
  		WebElement LoginButton =  driver.findElement(By.xpath("//button[@type='submit']"));
  		LoginButton.click();
  		Thread.sleep(2000);
  		}
		
		@Test(priority=5)
  	    //Click login Button
  		public void test5() throws InterruptedException {
  		WebElement Button =  driver.findElement(By.xpath("//button[@type='submit']"));
  		Button.click();
  		Thread.sleep(2000);
  		}

		@Test(priority=6)
		//HomePage title verify
		public void test6() throws InterruptedException {
		String HomePageTitle = driver.getTitle();
		System.out.println("The HomePage title is "+ HomePageTitle);
  		Thread.sleep(2000);
  		}

		@Test(priority=7)
		//Logo display verify
		public void test7() throws InterruptedException {
		Boolean logo = driver.findElement(By.xpath("(//img[@class='fl nLogo'])[1]")).isDisplayed();
		System.out.println(logo);
  		Thread.sleep(2000);
  		}
		
		@Test(priority=8)
  	    //Click Blogs
  		public void test8() throws InterruptedException {
  		WebElement Blogs =  driver.findElement(By.xpath("/html/body/main/div/div/div/div/div/div[2]/div/ul/li[4]/span"));
  		Blogs.click();
  		Thread.sleep(2000);
  		}

		@Test(priority=9)
  	    //Click search
  		public void test9() throws InterruptedException {
  		WebElement search =  driver.findElement(By.xpath("//span[@class='nI-gNb-sb__placeholder']"));
  		search.click();
  		Thread.sleep(2000);
  		}
		
		@Test(priority=10)
  	    //Enter Experience DropBox
  		public void test10() throws InterruptedException {
  		Select drpExperience =  new Select(driver.findElement(By.id("experienceDD")));
  		drpExperience.selectByIndex(2);;
  		Thread.sleep(2000);
  		}
		
		@Test(priority=11)
  	    //Enter Keywords
  		public void test11() throws InterruptedException {
  		WebElement Keyword =  driver.findElement(By.xpath("(//input[@class='suggestor-input '])[1]"));
  		Keyword.sendKeys("Software Automation Testing");
  		Thread.sleep(2000);
  		}
		
		@Test(priority=12)
  	    //Enter Keywords location
  		public void test12() throws InterruptedException {
  		WebElement location =  driver.findElement(By.xpath("(//input[@type='text'])[3]"));
  		location.sendKeys("Chennai");
  		Thread.sleep(2000);
  		}
		
		@Test(priority=13)
  	    //Click Submit
  		public void test13() throws InterruptedException {
  		WebElement Submit =  driver.findElement(By.xpath("//span[@class='ni-gnb-icn ni-gnb-icn-search']"));
  		Submit.click();
  		Thread.sleep(2000);
  		}
		
		@Test(priority=14)
		//To navigate to previous page 
		public void test14() throws InterruptedException {
		driver.navigate().back(); 
		Thread.sleep(1000);
		}
		
		@Test(priority=15)
		//Click to profile also screenshot
		public void test15() throws InterruptedException, IOException {
		WebElement profile =  driver.findElement(By.xpath("//a[@href='/mnjuser/profile']"));
	  	profile.click();
	  	
		TakesScreenshot TS = (TakesScreenshot)driver;
		File source = TS.getScreenshotAs(OutputType.FILE);
		File des = new File("C:\\Users\\dell\\Pictures\\Saved Pictures\\img.jpg");
		FileHandler.copy(source,des);
		}
		
		@AfterSuite
		@Test(priority=16)
		//Window close
		public void test16() {
		driver.quit();
		}
		
}


