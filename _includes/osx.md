## Mac OS X El Capitan (10.11)

There are two ways to trust the CAcert root certificates: one from the command line, and one from the Keychain GUI. Each method requires that you use an account with administrative privileges.

### Using the Keychain GUI

1. Download the desired certificate to a known location.
1. Open the certificate file, either using Command-O or by double-clicking on the file.
1. When Keychain appears, select "Add".
1. Search for the "Korcett Root Server" certificate in the list and double-click it.
1. Click in the Trust dropdown arrow.
1. Change the "Secure Sockets Layer (SSL)" option from "no value specified" to "Always Trust".
1. Close the window, you will be prompted to authenticate with your password to modify the Certificate Trust Settings.

### Using the command line

To import a trusted certificate use the following command:

{% highlight sh %}
sudo security add-trusted-cert -d -r trustRoot -k /Library/Keychains/System.keychain korcett-root-certificate.pem
{% endhighlight %}

This will add a trusted certificate to the System.keychain. You should modify the options and paths to suit your situation.

### Firefox troubleshoot

Firefox may not recognize the system certificate and still show a warning message for the user.

Follow the steps below to manually import the certificate:

1. Open Firefox preferences window (Command-,).
1. Navigate to Advanced > Certificates > View Certificates.
1. Select Authorities from the tabs and click Import.
1. Select the certificate and click Open.
1. Check "Trust this CA to identify websites." and click OK.
