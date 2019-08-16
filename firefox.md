# How to hide top tabs:

- Go to `about:config`
- Set `toolkit.legacyUserProfileCustomizations.stylesheets` to `true`
- Go to `about:support`
- Search for `Profile Directory` in that
- Create a `chrome` directory and create a `userChrome.css`
- Enter the following values in that file
```
/* hides the native tabs */
#TabsToolbar {
	visibility: collapse;
}

#titlebar {
	visibility: collapse;
}


#sidebar-header {
	visibility: collapse !important;
} 


/* leaves space for the window buttons */
#nav-bar {
    margin-top: -8px;
    margin-right: 74px;
    margin-bottom: -4px;
}

/* new tab colors */
@-moz-document url(about:blank) {
	html,body { background: black; }
}

@-moz-document url("about:newtab") {
	body { background-color: #303030 !important;}
}

/* Reduce the "white flash" in new tabs */
browser[type="content-primary"], 
browser[type="content"] {
  background: #778899 !important;
}

```
