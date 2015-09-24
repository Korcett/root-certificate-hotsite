## Ubuntu, Debian

1. Copy your CA to dir `/usr/local/share/ca-certificates/`.
1. Run the command:
  {% highlight sh %}
  sudo cp foo.crt /usr/local/share/ca-certificates/foo.crt
  {% endhighlight %}
3. Update the CA store:
  {% highlight sh %}
  sudo update-ca-certificates
  {% endhighlight %}

---

## CentOS 6

1. Install the ca-certificates package:
  {% highlight sh %}
  yum install ca-certificates
  {% endhighlight %}
1. Enable the dynamic CA configuration feature:
  {% highlight sh %}
  update-ca-trust enable
  {% endhighlight %}
1. Add it as a new file to `/etc/pki/ca-trust/source/anchors/`:
  {% highlight sh %}
  cp foo.crt /etc/pki/ca-trust/source/anchors/
  {% endhighlight %}
1. Run the command:
  {% highlight sh %}
  update-ca-trust extract
  {% endhighlight %}

---

## CentOS 5

Append your trusted certificate to file `/etc/pki/tls/certs/ca-bundle.crt`:
{% highlight sh %}
cat foo.crt >> /etc/pki/tls/certs/ca-bundle.crt
{% endhighlight %}
