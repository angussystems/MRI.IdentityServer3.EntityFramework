# EntityFramework Persistence Layer for IdentityServer3 #

Dev build: [![Build status](https://ci.appveyor.com/api/projects/status/e4t73mt1mid6vbdy?svg=true)](https://ci.appveyor.com/project/leastprivilege/thinktecture-identityserver-v3-entityframework)
[![Gitter](https://badges.gitter.im/Join Chat.svg)](https://gitter.im/IdentityServer/IdentityServer3?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)

IdentityServer3.EntityFramework is a persistence layer for IdentityServer v3 configuration data that uses EntityFramework as it's database abstraction. 

# Build procedure using power shell: #

NOTE: Assuming repository is checked out to C:\Development\MRI.IdentityServer3.EntityFramework folder

& "c:\Program Files\Microsoft Visual Studio\2022\Professional\MSBuild\Current\Bin\amd64\MSBuild.exe" /nologo C:\Development\MRI.IdentityServer3.EntityFramework\Source\IdentityServer3.EntityFramework.sln /p:Configuration=Release /p:TargetFrameworkVersion=v4.5
copy-item c:\Development\MRI.IdentityServer3.EntityFramework\build\IdentityServer3.EntityFramework.dll c:\Development\MRI.IdentityServer3.EntityFramework\distribution\lib\net45
copy-item c:\Development\MRI.IdentityServer3.EntityFramework\build\IdentityServer3.EntityFramework.pdb c:\Development\MRI.IdentityServer3.EntityFramework\distribution\lib\net45
copy-item c:\Development\MRI.IdentityServer3.EntityFramework\Source\IdentityServer3.EntityFramework.nuspec c:\Development\MRI.IdentityServer3.EntityFramework\distribution\

nuget.exe pack C:\Development\MRI.IdentityServer3.EntityFramework\distribution\IdentityServer3.EntityFramework.nuspec -BasePath C:\Development\MRI.IdentityServer3.EntityFramework\distribution -OutputDirectory C:\Development\MRI.IdentityServer3.EntityFramework\distribution -version 2.6.3

This should create a nuget package in the distribution folder of the repository.
