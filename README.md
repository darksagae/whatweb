# whatweb
**WhatWeb** is a web application fingerprinting tool included in Kali Linux. It is designed to identify various technologies used by a website, such as web servers, programming languages, frameworks, and other components.

### Installation

WhatWeb is typically pre-installed in Kali Linux. You can check if it's installed by running:

```bash
whatweb -v
```

If it’s not installed, you can install it using:

```bash
sudo apt update
sudo apt install whatweb
```

### Basic Usage

The basic syntax for using WhatWeb is:

```bash
whatweb [options] <target>
```

- `<target>`: Specifies the target URL or IP address to analyze.

### Example Commands

1. **Basic Scan**:
   To perform a basic scan on a website, use:

   ```bash
   whatweb http://example.com
   ```

2. **Verbose Mode**:
   For more detailed output, use the `-v` option:

   ```bash
   whatweb -v http://example.com
   ```

3. **Scan Multiple Targets**:
   You can scan multiple websites at once by providing a list:

   ```bash
   whatweb http://example1.com http://example2.com
   ```

4. **Using Plugins**:
   WhatWeb supports plugins for extended functionality. For example, to use the "all" plugin to identify all components:

   ```bash
   whatweb --plugin all http://example.com
   ```

### Expected Output

When you run WhatWeb, you can expect output similar to the following:

```
http://example.com [Apache] [WordPress] [PHP] [jQuery] [Google Analytics] [SSL]
```

In this output:

- `http://example.com`: The target URL.
- `[Apache]`: Indicates the web server being used.
- `[WordPress]`: Identifies the CMS.
- `[PHP]`: Shows the server-side language.
- `[jQuery]`: Indicates the JavaScript framework in use.
- `[Google Analytics]`: Indicates the presence of Google Analytics.
- `[SSL]`: Indicates that the site uses SSL for secure connections.

### Conclusion

WhatWeb is a valuable tool for reconnaissance, allowing you to quickly identify technologies in use on a web application. This information can be beneficial for security assessments and understanding the overall architecture of a target website. Always ensure you have permission to scan any web application to comply with ethical standards.



                         ALTERNATIVE
**WhatWeb** is a web application fingerprinting tool included in Kali Linux that identifies web technologies used by a website. It can detect various components such as content management systems, web servers, programming languages, and more.

### Installation

WhatWeb is usually pre-installed in Kali Linux. To check if it’s installed, run:

```bash
whatweb -v
```

If it’s not installed, you can install it using:

```bash
sudo apt update
sudo apt install whatweb
```

### Basic Usage

The basic command structure for WhatWeb is:

```bash
whatweb <target_url>
```

### Example Commands

1. **Basic Scan**:
   To perform a basic scan on a website:

   ```bash
   whatweb http://example.com
   ```

2. **Verbose Mode**:
   To get more detailed output during the scan, use:

   ```bash
   whatweb -v http://example.com
   ```

3. **Scan Multiple URLs**:
   You can scan multiple URLs by providing them in a file:

   ```bash
   whatweb -i urls.txt
   ```

4. **Scan with Specific Options**:
   To specify particular plugins or options, such as ignoring SSL errors:

   ```bash
   whatweb --ignore-ssl http://example.com
   ```

### Expected Output

The output from WhatWeb will typically include:

- **Detected Technologies**: A list of technologies and frameworks identified.
- **Version Information**: If available, it may show version numbers of detected components.

#### Example Output Snippet

When running a scan, you might see an output like this:

```
http://example.com
  HTTP Server: Apache/2.4.41
  Content-Type: text/html; charset=UTF-8
  CMS: WordPress
  Programming Language: PHP/7.4.3
  JavaScript Library: jQuery
```

### Conclusion

WhatWeb is a helpful tool for quickly identifying the technologies that a web application uses. This information can be valuable for security assessments and understanding the tech stack of a website. Always ensure you have permission to scan any web application to comply with legal and ethical standards.


                               ALTERNATIVE
WhatWeb is a web scanner tool included in Kali Linux. It is used to identify web technologies, including content management systems, blogging platforms, web frameworks, and more. Here's a brief overview of how to use WhatWeb and some examples:

**Basic Usage:**

The basic syntax for using WhatWeb is:
```
whatweb <target_url>
```
* `<target_url>`: Specifies the URL of the website you want to scan.

**Example Usage:**

1. **Basic Scan**:
```
whatweb http://example.com
```
This command will perform a basic scan of the `http://example.com` website and identify any web technologies it can detect.

2. **Verbose Mode**:
```
whatweb -v http://example.com
```
This command will run WhatWeb in verbose mode, providing more detailed output.

3. **Output to File**:
```
whatweb http://example.com -o output.txt
```
This command will save the scan results to a file named `output.txt`.

**Example Output:**

WhatWeb's output will typically include information about the web technologies detected, such as:
```
http://example.com [200] Apache/2.4.7, PHP/5.6.30, WordPress/4.9.8
```
In this example, WhatWeb has detected that the website is running Apache 2.4.7, PHP 5.6.30, and WordPress 4.9.8.

WhatWeb can also detect other web technologies, such as:

* Content management systems (e.g., Joomla, Drupal)
* Blogging platforms (e.g., WordPress, Blogger)
* Web frameworks (e.g., React, Angular)
* Server software (e.g., IIS, Nginx)
* And more

Keep in mind that WhatWeb is not a vulnerability scanner, but rather a tool for identifying web technologies. It can be useful for reconnaissance and information gathering during a penetration test or security assessment.





                          ALTERNATIVE
**whatweb - Web Application Fingerprinter**

whatweb is a web application fingerprinting tool included in Kali Linux. It is used to identify the technologies used by websites, such as content management systems, programming languages, JavaScript libraries, web servers, and more.

**Usage**

The basic syntax for using whatweb is:

```
whatweb [options] <target_url>
```

Some common options include:

- `-v`: Increase the verbosity of the output
- `-a <level>`: Set the aggression level (1-5, default is 3)
- `-c <color>`: Use colored output
- `-i <input_file>`: Scan a list of URLs from a file
- `-o <output_file>`: Save the results to a file

**Examples**

1. **Basic Scan**:
   ```
   whatweb http://example.com
   ```
   This will perform a basic scan of the `http://example.com` website and display the results in the terminal.

2. **Scan with Increased Verbosity**:
   ```
   whatweb -v http://example.com
   ```
   This will provide more detailed output about the technologies detected on the website.

3. **Scan with Aggressive Level**:
   ```
   whatweb -a 4 http://example.com
   ```
   This will perform a more aggressive scan, which may discover additional information about the website.

4. **Scan a List of URLs**:
   ```
   whatweb -i urls.txt
   ```
   This will scan the list of URLs provided in the `urls.txt` file.

5. **Save Output to a File**:
   ```
   whatweb -o report.txt http://example.com
   ```
   This will save the scan results to a file named `report.txt`.

**Example Output**

The output of a whatweb scan might look something like this:

```
http://example.com [200 OK] Apache[2.4.41], Country[RESERVED][ZZ], Email[someone@example.com], HTML5, HTTPServer[Apache/2.4.41 (Ubuntu)], IP[192.168.1.100], JQuery, PHP[7.4.3], Title[Example Domain], UncommonHeaders[link,x-pingback], X-Powered-By[PHP/7.4.3]
```

This output shows that the website running on `http://example.com` is using:

- Apache 2.4.41 web server
- PHP 7.4.3
- jQuery JavaScript library
- HTML5

The output also includes other information, such as the response status code, country, email address, and uncommon headers.

**Conclusion**

whatweb is a powerful tool for quickly identifying the technologies used by a website. By using various options, you can customize the scan to gather more detailed information about the target website. This information can be useful for security assessments, vulnerability testing, and understanding the technology stack of web applications.
