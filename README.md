wxWebViewWebKit2
================

wxWebViewwebKit2 is an experimental WebKitGTK+ WebKit2 backend. For more
detailed information, please see the project [wiki][1].

Requirements
------------

* [wxWidgets][2]: r73369 / 2.9.5  or greater
* [WebKitGTK+][3]:  2.0.0 or greater

Compiling
---------

This backend is made up of two files. Simply compile these alongside your
project and link again WebKitGTK.

Using
-----

To use wxWebViewChromium first register the backend with wxWidgets

    wxWebView::RegisterFactory(wxWebViewBackendWebKit2, 
                               wxSharedPtr<wxWebViewFactory>
                               (new wxWebViewFactoryWebKit2));

It can then be used in a standard `wxWebView::New` call

    wxWebView* webview = wxWebView::New(this, wxID_ANY,
                                        "http://www.wxwidgets.org/",
                                        wxDefaultPosition, wxDefaultSize,
                                        wxWebViewBackendWebKit2);

[1]: https://github.com/steve-lamerton/wxWebViewWebKit2/wiki
[2]: http://www.wxwidgets.org
[3]: http://webkitgtk.org

