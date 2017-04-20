# App_Browsers

A regularly updated collection of App\_Browsers configuration files for more accurate identification of User Agents/Web Browsers and Platforms/OS name and version information with ASP.NET 4+. These App\_Browsers files extend the existing .NET HttpBrowserCapabilities information to give a slightly more "user-friendly" name and version number. 

## Example Results

Browser Examples:

| Browser Used            | HttpBrowserCapabilities Reported Browser | Corrected Value w/ App_Browsers |
|-------------------------|------------------------------------------|---------------------------------|
| Microsoft Edge          | `Chrome`                                 | `Edge`                          |
| Seamonkey               | `Firefox`                                | `Seamonkey`                     |
| Maxthon                 | `Chrome`                                 | `Maxthon`                       |


Platform Examples: 

| Platform Used           | HttpBrowserCapabilities Reported Platform | Corrected Value w/ App_Browsers |
|-------------------------|-------------------------------------------|---------------------------------|
| Windows 10              | WinNT 10.0                                | Windows 10                      |
| Windows 8.1             | WinNT 6.3                                 | Windows 8.1                     |
| Windows Vista           | WinNT 6.0                                 | Windows Vista                   |
| Windows XP Professional | WinNT 5.2                                 | Windows XP Pro                  |

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

## Browser Identification Added

| Browser          | Version(s)                          | Issue          |
|------------------|-------------------------------------|----------------|
| Microsoft Edge   |                             Current |              - |
| Maxthon          |                             Current |              - |
| Seamonkey        |                             Current |              - |

## Platform Identification Added

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

## License

Licensed under the Apache License, Version 2.0 (the "License"). You may obtain a copy of the License in the LICENSE file, or at:

[http://www.apache.org/licenses/LICENSE-2.0](http://www.apache.org/licenses/LICENSE-2.0)

Unless required by applicable law or agreed to in writing, software distributed under the License is distributed on an "AS IS" BASIS, WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied. See the License for the specific language governing permissions and limitations under the License.
