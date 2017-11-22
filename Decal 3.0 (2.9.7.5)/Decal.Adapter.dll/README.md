# Decal 3.0 (2.9.7.5) / Decal.Adapter.dll

**This dll affects .net based plugins in the following ways:**
* Requesting item information via RequestId() will no longer take a minimum of 600ms. The minimum is now 10ms.

## Install Instructions
* Close Decal if it's running.
* Locate your Decal installation folder, typically: "C:\Program Files (x86)\Decal 3.0\"
* Rename your original Decal.Adapter.dll to Decal.Adapter.dll.orig
* Download the Decal.Adapter.dll in this repository and copy it to the following 2 locations:
* Your Decal installation folder, typically: "C:\Program Files (x86)\Decal 3.0\"
* Your Asheron's Call installation folder, typically: "C:\Turbine\Asheron's Call"
* Start Decal.

## Troubleshooting
#### 1. acclient has stopped working
* _Problem_
> When launching the client, you're immediately presented with a crash. Problem details show the "Fault Module Name" is decalnet.dll. This is because decalnet.dll cannot find Decal.Adapter.dll. We haven't registered the new modified dll. decalnet.dll is still looking for the old one. Because the client isn't starting up in the Decal 3.0 folder, it doesn't search that folder for our modiified dll.
* _Solution_
> Copy the modified Decal.Adapter.dll to the Asheron's Call installation folder.

## Tools I Used
* I used [dnSpy](https://github.com/0xd4d/dnSpy) to remove the Strong-Name signature as well as patch in my changes.

## Credits
* Hazridi for granting me the permission to do this.
* Virindi for pointing me to the exact location of the code.
* parad0x for helping me through com interface issues after the dll was modified.
* Hellswrath for being my first tester.