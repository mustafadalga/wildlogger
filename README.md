```

 __          ___ _     _    _
 \ \        / (_) |   | |  | |
  \ \  /\  / / _| | __| |  | |     ___   __ _  __ _  ___ _ __
   \ \/  \/ / | | |/ _` |  | |    / _ \ / _` |/ _` |/ _ \ '__|
    \  /\  /  | | | (_| |  | |___| (_) | (_| | (_| |  __/ |
     \/  \/   |_|_|\__,_|  |______\___/ \__, |\__, |\___|_|
                                         __/ | __/ |
                                        |___/ |___/

```

### Description
 A keylogger designed for Windows operating system that captures connection information, device system information, a list of running processes and stopped services on the operating system, keyboard keystrokes, copy-paste clipboard content, and screenshots of the target system, sending them to a specified email address at specified time intervals.

### Details

<table>
 <tr>
  <td>
   :arrow_right:
  </td>
  <td>
 2 different threads are used to send log records and screenshots as reports; 
 <p>:heavy_check_mark:1.thread sends log records to the specified email address based on the specified time interval.   </p>
 <p>:heavy_check_mark: 2.thread takes screenshots at specified intervals. If the number of screenshots taken reaches 10, it reports the screenshots to the specified email address and deletes them to avoid detecting anomalies on the target computer.</p>
  </td>  
 </tr>
   <tr>
  <td>
   :arrow_right:
  </td>
   <td>
By default, Google Mail server is used for reporting operations.  
  </td>  
 </tr>
 <tr>
   <td>
   :arrow_right:
  </td>
 <td>
  If reporting is to be done using Gmail SMTP server, <a href="https://www.google.com/settings/security/lesssecureapps" alt="Less secure app access">Less secure app access</a> must be enabled.
 </td>
 </tr>
  <tr>
    <td>
   :arrow_right:
  </td>
 <td>
  The <strong>persistent</strong> method, which ensures Wildlogger continuously runs on the target computer, is deactivated by default.
 </td>
 </tr>
 <tr>
    <td>
   :arrow_right:
  </td>
 <td>
  When Wildlogger is converted to an exe, the <strong>persistent</strong> method must be activated for it to run continuously on the target computer. After the <strong>persistent</strong> method is activated;  
<p>:heavy_check_mark: The executed Wildlogger file is copied to the appdata folder with the name "Windows Explorer",  </p>
<p>:heavy_check_mark: In the registry, persistence is ensured by adding the keylogger file's path among the applications that run at Windows startup.</p>
 </td>
 </tr>
 </table>


### Modules to install for usage
* Windows installation
```
python -m pip install -r .\requirements.txt
```

### Usage
```
python wildlogger.py 
```
