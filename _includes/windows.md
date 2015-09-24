## Windows

### Using the command line

To import a trusted certificate use the following command:

{% highlight sh %}
certutil -addstore -f "ROOT" new-root-certificate.crt
{% endhighlight %}
