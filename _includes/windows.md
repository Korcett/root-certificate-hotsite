## Using the command line (Windows 7/8/8.1/10)

Open the Command Prompt as Administrator and follow these steps.

Navigate to where the file is located (Usually the Downloads folder, replace Username with your local Windows user):
{% highlight sh %}
dir c:\Users\Username\Downloads
{% endhighlight %}

Run the following command:
{% highlight sh %}
certutil -addstore -f "ROOT" korcett-root-certificate.pem
{% endhighlight %}

---

## Windows 8/8.1/10

1. Double click the file (korcett-root-certificate.pem).
2. Click **Install certificate**.
3. Store location: Keep **Current user** or select **Local machine** to install for all users.
4. Certificate store: Click **Place all certificates in the following store** and select **Trusted Root Certification Authorities**.
5. Complete the Wizard.

---

## Windows 7

To add certificates to the Trusted Root Certification Authorities store for a local computer:

1. Click **Start**, click **Start Search**, type **mmc**, and then press ENTER.
1. On the **File** menu, click **Add/Remove Snap-in**.
1. Under **Available snap-ins**, click **Certificates**, and then click **Add**.
1. Under **This snap-in will always manage certificates for**, click **Computer account**, and then click **Next**.
1. Click **Local computer**, and click **Finish**.
1. If you have no more snap-ins to add to the console, click **OK**.
1. In the console tree, double-click **Certificates**.
1. Right-click the **Trusted Root Certification Authorities** store.
1. Click **All Tasks > Import** to import the certificates and follow the steps in the Certificate Import Wizard.
1. In the file browser dialog box change the extension to **All Files (\*.\*)** to select the file, click **Open** and then **Next**.
1. In the **Certificate Store** step, make sure that **Place all certificates in the following store** is checked and **Trusted Root Certification Authorities** is selected, then click **Next**.
1. Click **Finish**.
1. You may now close the **Console Root** window, select **No** when prompted to save the console changes.
