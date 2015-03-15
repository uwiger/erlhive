# Introduction #

There are lots of things to do with Erlhive. This page tries to list the most important ones. Please feel free to contribute.


# TO-DO List #

## Template support ##

From what we can tell the Erlang [stringtemplate](http://www.stringtemplate.org) engine, [sgte](http://code.google.com/p/sgte/), works in Erlhive. There are some things to address:

  * Should Erlhive have a generic template API? (yaws\_tei was suggested as a model)
  * Shouldn't e.g. the blog example be ported to sgte templates?

## [OpenSocial](http://code.google.com/apis/opensocial/) ##

This is a set of APIs for clients and servers, aiming at making it easier
to collaborate on the web. At first glance, the server-side functionality
should be really easy to support in Erlhive.

## [WebDAV](http://www.webdav.org) ##

I've not worked with WebDAV before, but browsing through some docs,
it seems as if Erlhive natively supports many of the things that are
needed for WebDAV:

  * File system support
  * Meta-data - all Erlhive object can have meta-data
  * Access control

Long-duration locks is something that needs looking into. An easy way to
do it would be to use Erlhive's internal object properties (which can be
manipulated only by trusted code).

## Parser and rendering libraries ##

One of Erlhive's strengths is that it allows for a collection of
server-side reusable libraries. I'd like to see some libraries for
parsing specialized Wiki syntax, e.g. for on-line slide shows, documents,
code contributions, etc.

Why not have modules that offer both an API for parsing Wiki text and
expanding the result with appropriate templates?

## Example applications ##

First of all, the blog example should be completed. There are several
things supported in the back-end module that cannot be accessed from
the web interface.

## Interactive shell ##

The interactive shell seems to work, but it would be very nice to
be able to use it via SSL against a live system. A Flash telnet
client (http://flashforever.homeip.net/blog/?p=13) might be just the
thing to make this happen.