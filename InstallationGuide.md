# Installation #

Unlike INDE v1, INDE v2 does not include an installer, instead follow the few steps below to install and configure INDE2 for your system.

  1. Unzip `inde2.zip` and place it in your `/Applications directory` (e.g. `/Applications/inde2/`).
  1. Inside the `inde2` directory you will find a folder named `FDTTemplates`. Copy `FDTTemplates` to: `/Users/your-username/Library/Application Support/`.
  1. Rename `/Users/your-username/Library/Application Support/FDTTemplates`to `/Users/your-username/Library/Application Support/FDT`.
  1. Next we will configure your Apache Webserver to point to the **INDE2 workspace**: Open `Terminal.app` & type `sudo nano /etc/apache2/httpd.conf`.
  1. Locate the `DocumentRoot` line in your conf file (e.g. `DocumentRoot "/Library/WebServer/Documents"`).
  1. Change this line to read `DocumentRoot "/Applications/inde2/workspace"`.
  1. Locate the `Directory` line in your conf file (e.g. `<Directory "/Library/WebServer/Documents">`).
  1. Change this line to read `<Directory "/Applications/inde2/workspace">`.
  1. Within the `<Directory>` node insure/change the `AllowOverride` to read: `AllowOverride All`.
  1. Now locate the line that reads `Include /private/etc/apache2/extra/httpd-vhosts.conf` - comment this line out by putting a `#` character in front of it (e.g. `#Include /private/etc/apache2/extra/httpd-vhosts.conf`).
  1. FInally, save the httpd.conf file by typing `Control+X`then `Y` to save the file.
  1. Lastly, restart apache by typing `sudo apachectl graceful` into`Terminal.app`.
  1. Now navigate to `http://localhost/` and you should see your prettified INDE2 workspace:

![http://inde.sekati.com/lib/branding/collateral/inde2/workspace.png](http://inde.sekati.com/lib/branding/collateral/inde2/workspace.png)

  1. You are now ready to Launch **inde2.app**, enter your FDT4 License Key and begin development. Please refer to the [Documentation Wiki](http://code.google.com/p/inde/wiki/Documentation) for more information!