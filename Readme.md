
This version of Finagle Thrift has been shamelessly forked from
https://github.com/twitter/finagle.

Twitter seems to have lost interest in updating the
Ruby version of Thrift to the point of the code having some deprecations
from the Ruby interpreter which can be quite annoying when they are
logged or otherwhise pollute the output.

This repo has version 1.3.2 which is greater than 1.3.1, the last
version published by Twitter.
As zipkin related tech depends on '~> 1.3.1', it  means that if you point to
this repository's '1.3.2' tag, you will be using this code instead of
the official Twitter's.

I've in fact not modified twitter's code. They have the problem solved
in their repo but never released the gem. The reason you can't just
point to Twitter's repo and be done with it is that they have one repo
to host several projects and programming languages, that's not how
bundle or gem works.

In summary, to avoid those pesky Hash#index deprecation warnings, do
this in your gemfile:

```Ruby
gem 'finagle-thrift', git: 'git@github.com:JordiPolo/finagle-thrift',
tag: '1.3.2'
```
