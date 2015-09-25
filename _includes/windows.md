## Windows

1. Double click the file (korcett-root-certificate).
2. Click "Install certificate".
3. Store location: Keep "Current user" or select "Local machine" to install for all users.
4. Certificate store: Click "Place all certificates in the following store" and select "Trusted Root Certification Authorities".
5. Complete the Wizard.

### Using the command line

Open the Command Prompt as Administrator and run the following command:

{% highlight sh %}
certutil -addstore -f "ROOT" korcett-root-certificate.pem
{% endhighlight %}
