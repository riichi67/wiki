# 🤖 Theme Format

```json
{
name: string;
description: string;
authors: [ 
	{
		 name: string;
		 id: string;
	}
],
spec: 2;
semanticColors: { 
    "key: string": "[ string, string, string ]"
	// [ Dark theme, light, amoled ]
			// all #hex        
};
rawColors: { 
    "[ key: string ]": "string"
	// #hex
},
"background": {
    "blur": 0.1, // background blur
    "url": "image link",
    "alpha": 1.0 // background opacity
    },
}
```

Color codes inside the `semanticColors` and `rawColors` object can be the following:

* 6 character HEX --> `#RRGGBB`
  * Don't put the alpha values `(#RRGGBBAA)` in **rawcolors** because it might crash discord
* CSS `rgba()` --> `rgba(0, 0, 0, 1)`
  * **\[ ! ]** `rbga()` needs to follow the above format exactly. You **cannot** use `rgba(r g b a)` or `rgba(r g b / a)`
* A `transparent` string can also be used

### Example:

```json
{
	name:Lavender Heaven;
	description: A theme made by Vodka;
	authors: [ 
	{
			name: Vodka Martini;
		  id: 1068030255455015013;
	}
],
spec: 2;
semanticColors: { 
							"HEADER_PRIMARY":  ["#EFDFD7", "#E7D6CE", "#A07D6C"]
									                  //Dark theme, light, amoled         
};
rawColors: { 
					"PRIMARY_500": "#9E8376"
},
"background": {
    "blur": 0.6,
    "url": "https://cdn.discordapp.com/attachments/1086985889286209586/1099189661995380897/82ef73f876a5ef467a8263b694e4f0b8.jpg",
    "alpha": 0.4
    },
}
```
