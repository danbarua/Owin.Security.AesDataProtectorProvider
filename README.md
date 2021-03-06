.NET (4.5) [![Build status](https://ci.appveyor.com/api/projects/status/0vjtl572q4f8nh3r/branch/master)](https://ci.appveyor.com/project/i4004/owin-security-aesdataprotectorprovider/branch/master) Mono (3.8.0) [![Travis build status](https://travis-ci.org/i4004/Owin.Security.AesDataProtectorProvider.png?branch=master)](https://travis-ci.org/i4004/Owin.Security.AesDataProtectorProvider)

[![Nuget version](http://img.shields.io/badge/nuget-v1-blue.png)](https://www.nuget.org/packages/Owin.Security.AesDataProtectorProvider/)
[![NuGet Status](http://nugetstatus.com/Owin.Security.AesDataProtectorProvider.png)](http://nugetstatus.com/packages/Owin.Security.AesDataProtectorProvider)
 [![Stories in Ready](https://badge.waffle.io/i4004/Owin.Security.AesDataProtectorProvider.png?label=ready&title=Ready)](https://waffle.io/i4004/Owin.Security.AesDataProtectorProvider)

---

Owin.Security.AesDataProtectorProvider
============

`Owin.Security.AesDataProtectorProvider` - is an AES cryptic provider for OWIN autnetication middlewares.

Available at NuGet as [binary package](https://www.nuget.org/packages/Owin.Security.AesDataProtectorProvider/)

### Registration

```csharp
public class Startup
{
	public void Configuration(IAppBuilder app)
	{
		...
		app.UseAesDataProtectorProvider();
		...
	}
}
```

### Usage example with cookie authentication


```csharp
public class Startup
{
	public void Configuration(IAppBuilder app)
	{
		app.UseCookieAuthentication(new CookieAuthenticationOptions
		{
			AuthenticationType = DefaultAuthenticationTypes.ApplicationCookie,
			LoginPath = new PathString("/login")
		});

		app.UseAesDataProtectorProvider();
	}
}
```
