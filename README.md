# MFC_webBrowser

[ *MAKE A NEW DIALOG BASED PROJECT* ]

![image](https://user-images.githubusercontent.com/61898376/153789037-c554ca32-c75d-4211-abfb-de1b14f245a0.png)

![image](https://user-images.githubusercontent.com/61898376/153789146-546d74c1-42ef-41ba-ad47-c253af9c2243.png)

![image](https://user-images.githubusercontent.com/61898376/153789265-725d61c0-08c4-4aa6-88d1-ffde7c255517.png)

-----

[ *Go to resource file >> dialog >> mouse Right click >> add ActiveX Control* ]

![image](https://user-images.githubusercontent.com/61898376/153789342-32604b07-4df3-4a0f-b0b4-076d5b1c1db3.png)


[*choose web browser*]

![image](https://user-images.githubusercontent.com/61898376/153789517-04e1c1bd-6f82-488a-af56-54aa0dbb1481.png)

[*click Save*]

![image](https://user-images.githubusercontent.com/61898376/153789627-e52671af-42aa-48fe-9e1a-6d7657d5e0b5.png)


-----
[ *while pressing ctrl -> mouse double click* ]

![image](https://user-images.githubusercontent.com/61898376/153790047-f2b671b7-66bd-48e5-9ab5-5c31b8c3ca04.png)
![image](https://user-images.githubusercontent.com/61898376/153790169-851bd9f0-abe4-432a-88cc-ee42f10c0bde.png)

-----
![image](https://user-images.githubusercontent.com/61898376/153790223-c61eb704-2743-4364-91ef-ed4225541709.png)

[*open Explorer1.h file >> add those line of codes*]
```
void Navigate(LPCTSTR URL, VARIANT * Flags, VARIANT * TargetFrameName, VARIANT * PostData, VARIANT * Headers)
	{
		static BYTE parms[] = VTS_BSTR VTS_PVARIANT VTS_PVARIANT VTS_PVARIANT VTS_PVARIANT;
		InvokeHelper(0x68, DISPATCH_METHOD, VT_EMPTY, NULL, parms, URL, Flags, TargetFrameName, PostData, Headers);
	}
```
![image](https://user-images.githubusercontent.com/61898376/153790343-c0915344-e355-4466-9b10-553b4eced0bc.png)

[ *check DDX_control if new m_web is added* ]

![image](https://user-images.githubusercontent.com/61898376/153790542-5d703ae8-e95f-439d-a4a8-0bea6a037ea1.png)

[ *call Navigate function, add an url as an argument* ]

![image](https://user-images.githubusercontent.com/61898376/153790786-e000eb94-4e6f-4568-81e6-704a09604b24.png)

[ *RESULT* ]

![image](https://user-images.githubusercontent.com/61898376/153790874-4ebeb4b2-e124-4b53-9f14-b5838af08c74.png)


