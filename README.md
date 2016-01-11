


> Written with [StackEdit](https://stackedit.io/).

System.getProperties().getProperty("browser")


Run/Debug Configurations->Defaults->Junit->VM options
-Dbrowser=FIREFOX
-Dbrowser=CHROME
-Dbrowser=IE
-Dbrowser=SAFARI


 public static void openBrowser(String url) {
  if (System.getProperties().getProperty("browser").equals("FIREFOX")) {

            FirefoxProfile profile = new FirefoxProfile();
            profile.setAcceptUntrustedCertificates(true);
            driver = new FirefoxDriver(profile);
            driver.get(url);

        } else if (System.getProperties().getProperty("browser").equals("CHROME")) {
....
...


Example:
maven clean test -Dbrowser=FIREFOX