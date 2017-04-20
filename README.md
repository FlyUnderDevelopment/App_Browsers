# App_Browsers

A regularly updated collection of App\_Browsers files for more accurate identification of User Agents/Web Browsers and Platforms/OSes with ASP.NET 4+. These App\_Browsers files extend the existing .NET HttpBrowserCapabilities information to give a slightly more detailed name and version number. 

## Installation

### Visual Studio 2015

To add App\_Browsers to your ASP.NET Web application:

1. Right-click on your project and choose **Add > Add ASP.NET Folder > App\_Browsers**
2. **Copy the \*.browser files to** the newly created **App\_Browsers** folder
3. Modify your **Web.config** file by additing the following line of code:

#### Web.config
    ```
    <system.web>
        ...
        <browserCaps userAgentCacheKeyLength="256" />
        ...
    </system.web>
    ```

## Usage

Within your action you can access the updated browser/platform information by adding:

```
    System.Web.HttpBrowserCapabilities _browser = System.Web.HttpContext.Current.Request.Browser;
    Debug.WriteLine("Name: " + _browser.Browser);
    Debug.WriteLine("Platform: " + _browser.Platform);
```

## Additional Browser Identification Added

| Browser          | Version(s)                          | Issue          |
|------------------|-------------------------------------|----------------|
| Microsoft Edge   |                             Current |              - |
| Maxthon          |                             Current |              - |
| Seamonkey        |                             Current |              - |

## Additional Platform Identification Added

| Platform         | Version(s)                          | Issue          |
|------------------|-------------------------------------|----------------|
| Windows          |                                     |              - |
|                  | Windows 10                          |              - |
|                  | Windows 8.1                         |              - |
|                  | Windows 8                           |              - |
|                  | Windows 7                           |              - |
|                  | Windows Vista                       |              - |
|                  | Windows XP Pro                      |              - |
|                  | Windows XP                          |              - |