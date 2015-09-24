## Ubuntu, Debian

1. Copy your CA to dir `/usr/local/share/ca-certificates/`.
1. Run the command:
  {% highlight sh %}
  sudo cp korcett-root-certificate.pem /usr/local/share/ca-certificates/korcett-root-certificate.pem
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
  cp korcett-root-certificate.pem /etc/pki/ca-trust/source/anchors/
  {% endhighlight %}
1. Run the command:
  {% highlight sh %}
  update-ca-trust extract
  {% endhighlight %}

---

## CentOS 5

Append your trusted certificate to file `/etc/pki/tls/certs/ca-bundle.crt`:
{% highlight sh %}
cat korcett-root-certificate.pem >> /etc/pki/tls/certs/ca-bundle.crt
{% endhighlight %}
