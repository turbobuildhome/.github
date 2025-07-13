## Welcome To Turbobuild

TurboBuild is a build acceleration tool.  
It can significantly reduce compilation time, at least by more than half.   
Doesn't require you to do anything, just a config file. It works just fine.  
If you work on windows, use mscv. It's the only free tool that can do it. 
  

## How to use

[Download Zip](https://github.com/turbobuildhome/turbobuild)

buildassist.exe => build task access，adaptation to different build tools, vs\cmake\ninja. 
captain.exe => Cluster Manager   
crew.exe => Cluster worker   
cocrew.exe => Cluster worker second  
redirect64.dll  

### step 1.  
Run the program you need

first run captain.exe on the any device you need, it is a management service.  
acceptance of crew.exe registration. 


### step 2.
Second run crew.exe with -h args pass addr registe to captain.exe.

crew.exe -h 192.168.2.1 indication that connect to captain.exe run on 192.168.2.1 devices.

step 3.  
choose your opened sloution type.  
1> Visual Studio Sloution  
just add a Directory.Build.props xml config file into your sloution file path.

Directory.Build.props
```xml
<Project>
  <PropertyGroup>
	<CLToolExe>buildassist.exe</CLToolExe>
	<CLToolPath>D:\turbobuild</CLToolPath>
  </PropertyGroup>
</Project>
```
you just simply need modify CLToolPath item, use your actual local buildassist.exe path.  

When you build again, the task has been quietly distributed to all the worker nodes in the cluster.

  
## Cloud process technology
The local process can run on any accessible device, just as it would run locally. 
The result of the execution is exactly the same as that of the local execution.
Based on this technology. The compilation process can be moved to any device within the cluster.
Therefore, as long as the number of CPU cores in the cluster is sufficiently large, the number of concurrent compilations can approach the limit. and the compilation time can approach the minimum.
<!--

## Report Issue
https://github.com/turbobuildhome/turbobuild/issues

**Here are some ideas to get you started:**

🙋‍♀️ A short introduction - what is your organization all about?
🌈 Contribution guidelines - how can the community get involved?
👩‍💻 Useful resources - where can the community find your docs? Is there anything else the community should know?
🍿 Fun facts - what does your team eat for breakfast?
🧙 Remember, you can do mighty things with the power of [Markdown](https://docs.github.com/github/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax)
-->
