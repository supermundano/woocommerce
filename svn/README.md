# SVN Instructions

This file explains how to upload a new module version to Woocommerce market.

## Upload

1- Located in your local Woocommerce root folder, clone Pagantis svn repository:
```
svn checkout http://plugins.svn.wordpress.org/pagantis svn/
```

2- Move the current code to the current tag version
```
mkdir svn/tags/<current_version>
cp -pr svn/trunk/ svn/tags/<current_version>
```

3- Remove old content inside trunk folder
```
rm -rf svn/trunk/*
```

4- Copy new files to trunk, overwriting the old one.
```
cp -pr assets/ svn/trunk/assets/
cp -pr controllers/ svn/trunk/controllers/
cp -pr includes/ svn/trunk/includes/
cp -pr languages/ svn/trunk/languages/
cp -pr templates/ svn/trunk/templates/
cp -pr vendor/ svn/trunk/vendor/
cp readme.txt svn/trunk/readme.txt
cp WC_Pagantis.php svn/trunk/WC_Pagantis.php
``` 

4- Add the files to svn track
```
svn add --force svn/.
```

5- Commit the files to svn
```
svn commit -m "<new_version>"
```  

6- Fill username and password
