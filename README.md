//Alerts
Alert alert= driver.switchTo().alert();
alert.accept();
alert.dismiss();
alert.sendkeys("hi");
alert.getText();
//Alert using explicit wait
WebDriver wait= new WebDriverWait(driver,10);
Alert alert= wait.until(ExpectedConditions.alertsIsPresent());
alert.accept();


//Frames
driver.switchTo().frame(0); //using Index
driver.switchTo().frame(framename/frameID); //using frame name/id
driver.switchTo().frame(iframeElement);//using iframeElement
driver.switchTo().parentFrame();//switch to parent window
driver.switchTo().defaultContent();// switch back to normal content/main page
//Find the count of iFrames
List<WebElement> frames= driver.findElements(By.tagName("iframe"));
System.out.println("iframe.size()");
// Switch to the outer iframe
driver.switchTo().frame("outerIframeId");
// Switch to the inner iframe within the outer iframe
driver.switchTo().frame("innerIframeId");
driver.switchTo().parentFrame();
driver.switchTo().defaultContent();


//dropdown
WebElement dropDown= driver.findElement(By.xpath(""));
Select dp=new Select(dropDown);
dp.selectByindex(0);
dp.selectByValue("selectByValue1");
dp.selectByVisibleText("option1");
dp.getFirstSelectedOption();
//get all the options: for each loop
WebElement dropDown= driver.findElement(By.xpath(""));
Select dp=new Select(dropDown);
List<WebElement> allOptions= dp.getOptions();//dropdown.getOptions() retrieves all the options inside the dropdown as a List<WebElement>.
for(webElement slectdd: allOptions)
{
  System.out.println(slectdd.getText());
}

//windows handle
String currentWindow=driver.getwindowHandle();
//window handles using iterator
Set<String> allWindows=driver.getwindowHandles();
Iterator it=allWindows.iterator();
while(it.hasNext())
{
  String currentWindow=it.next();
  driver.switchTo().window(currentWindow);
  System.out.println(driver.getTitle());
}

//Excel
File f= new File("");
Workbook bk= new XSSFWorkbook(bk);
Sheet sh= bk.getSheet("datasheet");
Row r= sh.getRow(0);
String cellValue= r.getCell(0).getStringCellValue();
// for sheet numbers
int sheet = bk.getNumberOfSheets();
//for sheet name
String sheetName= bk.getSheetName(i);
//number of rows
int rowCount= getPhysicalNumberOfRows();
//number of columns
int colCount=r.getLastCellNum();

//Property File
FileReader reader= new FileReader();
Properties prop= new Properties();
prop.reader(reader);
String value= prop.getProperty("");

//parameters
<parameter name="" value=""/>
@Parameters({"name"})
public void parameterizedTest(String myName)
{
  
}

//Screenshot
TakesScreenshot tb= (TakesScreenshot(driver));
File src= tb.TakesScreenshotAs(Output Type.File);
File des= new File("");
FileUtils.copyFile(src,des);

//Extent Report
String path=System.setProperty("path");
ExtentSparkReporter report= new ExtentSparkReporter(path);

ExtentReports extent = new ExtentReports();
extent.attachReporter(report);
ExtentTest test = new extent.createTest("initial demo");
extent.flush();

//Actions Class
Actions action = new Actions();
action.moveToElement(element).perform();
action.ContextClick(Element).perform();
action.doubleClick(Element).perform();
action.dragAndDrop(source, target).perform();
action.keyDown(keys.CONTROL).sendKeys("t").keyUp(Keys.CONTROL).perform();


//Waits;
WebDriver wait= new WebDriverWait(driver, 10);
wait.unitl(ExpectedConditions.visibilityOf(element))


driver.manage().implicityWait(10, TimeUnit.Seconds);

//javascript Executor
JvaScriptExecutor js= JavascriptExecutor(driver);
js.executescript("window.scrollBy(0,500)");//scroll to the bottom
js.excecutescript("window.scrollBy(0,0)");//scroll to the top
js.exceutescript("window.scrollBy(0,500)"); scroll to the horizontal
js.excecuteScript("argument[0].scrollintoview(true);", element)

