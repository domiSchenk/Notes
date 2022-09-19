---
id: 2zu0qikr1e0bd7fvo3ezt0y
title: Reinstall nugets
desc: ''
updated: 1663575853557
created: 1663575853557
---

# Force Nuget to Reinstall Packages without Updating

Occasionally I run into an issue where I’ll open a solution in Visual Studio, build it, and the build will fail because of dependent packages. I’ll try every way offered by Visual Studio to restore packages, but it will claim everything is up to date. Looking in Solution Explorer, you’ll see that some packages are clearly missing (icons on the packages showing they’re not there), but no amount of telling VS to restore packages (or building, which should do the restore as well) will get them.

The fix for this is to open Package Manager Console and run this command:

```bash
Update-Package -reinstall
```

Note: If you just run Update-Package, it will try to update all packages to the latest version, which isn’t necessarily what you want (especially if you’ve simply pulled from source control and want the project to just build with the versions of packages it has in source control).

That’s it – this does the trick for me. If you want to narrow it down to a certain project, just make sure you’ve selected the correct active project, or use this:

```bash
Update-Package -reinstall -Project ProjectName
```


## Source
Link: https://ardalis.com/force-nuget-to-reinstall-packages-without-updating/