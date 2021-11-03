# AGPLibResourcesBug
Sample app demonstrating bug in AGP resource caching when using resValue field in a library module.

Verify bug by running:
```
./gradlew bundleLibResDevRelease
./gradlew bundleLibResProdRelease
```

And checking the generated resource files. You'll see that the second task (bundleLibProdRelease) will use cached results from the first task, even if that is invalid.
