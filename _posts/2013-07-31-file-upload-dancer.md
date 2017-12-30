---
layout: post
title:  "File Upload using Perl and DANCER"
date:   2013-07-31
categories: programming perl dancer file upload
---

One of the most common functions in a web application is File Upload. The following is a working code that can be used to this end. The prerequisites are only Perl (obviously) and the DANCER framework. Right! Here goes:

```
post '/upload/:file' =&gt; sub {
  my $upload_dir = "/home/fpsom/myApp/UPLOADS";
  my $filename = params-&gt;{file};
  my $uploadedFile = upload('file_input_foo');
  $uploadedFile-&gt;copy_to("$upload_dir/$filename");
  debug "My Log 1: " . params-&gt;{file};
  debug "My Log 2: " . ref($uploadedFile);
};
```

This should be copied in the `myApp/lib/myApp.pm` file (check for the corresponding file in your app)

In order to check the functionality of this code, I've used `cURL` as follows, where `testUploadFile` is an existing file:

```
curl -i -F file_input_foo=@testUploadFile http://localhost:3000/upload/testUploadFile
```

The output on the "development dance floor" should be as follows:

```
[10269]  core @0.000119&gt; request: POST /upload/testUploadFile from 127.0.0.1 in /usr/local/share/perl/5.14.2/Dancer/Handler.pm l. 56
[10269]  core @0.000413&gt; [hit #4]Trying to match 'POST /upload/testUploadFile' against /^\/upload\/([^\/]+)$/ (generated from '/upload/:file') in /usr/local/share/perl/5.14.2/Dancer/Route.pm l. 84
[10269]  core @0.000530&gt; [hit #4]  --&gt; got 1 in /usr/local/share/perl/5.14.2/Dancer/Route.pm l. 102
[10269]  core @0.000627&gt; [hit #4]  --&gt; named tokens are: file in /usr/local/share/perl/5.14.2/Dancer/Route.pm l. 130
[10269] debug @0.001051&gt; [hit #4]My Log 1: testUploadFile in /home/fpsom/myApp/lib/myApp.pm l. 21
[10269] debug @0.001145&gt; [hit #4]My Log 2: Dancer::Request::Upload in /home/fpsom/myApp/lib/myApp.pm l. 22
[10269]  core @0.001446&gt; [hit #4]response: 200 in /usr/local/share/perl/5.14.2/Dancer/Handler.pm l. 179
```

And that is that! Hope it helps.

{% include  share.html %}
