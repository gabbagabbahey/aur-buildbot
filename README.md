aur-buildbot
============

This shell script automates process of updating VCS-based packages (e.g., -git, -svn, -hg) that feature extremely frequent changes that typically don't require manual intervention.

*Usage (w/ upload to AUR):*
```
aur-buildbot PKGNAME AUR__USERNAME AUR__PASSWORD
```

*Usage (w/o upload to AUR):*
```
aur-buildbot PKGNAME
```

*How it works:* 
- Download current PKGBUILD (wget/tar)
- Check for newer commit (makepkg)
- Build new version (makepkg)
- Check package for errors (namcap)
- Build source package (mkaurball)
- Upload source package to AUR (burp)

