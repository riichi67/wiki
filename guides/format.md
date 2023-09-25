# 🤖 Theme Format

```ts
interface Theme {
  /** Theme's name */
  name: string;
  /** Theme's description */
  description: string;
  /** Array of theme authors */
  authors: {
    /** Author's nickname */
    name: string;
    /** Author's Discord user ID */
    id: string;
  }[];
  /** Theme version (currently 2) */
  spec: 2;
  /** Object containing the semantic color recolorations */
  semanticColors: {
    /** Semantic key */
    [semanticKey: string]: [
      /** Dark HEXA color */
      string,
      /** Light HEXA color */
      string,
      /** Amoled HEXA color */
      string
    ];
  };
  /** Object containing the raw color recolorations */
  rawColors: {
    [key: string]: string;
  };
  /** Background that shows up in chat */
  background: {
    /** Determines the blurriness of the background (goes from 0-1) */
    blur: number;
    /** A link to the background */
    url: string;
    /** Determines the opacity of the background (goes from 0-1, affects color too) */
    alpha: number;
  };
}
```

Color codes inside the `semanticColors` and `rawColors` object can be the following:

- 3/6 character HEX --> `#RGB(A)` or `#RRGGBB(AA)`
  - Alpha is optional, may crash discord if used in a `rawColor`
- CSS `rgba()` --> `rgba(0, 0, 0, 1)`
  - **\[ ! ]** `rbga()` needs to follow the above format exactly. You **cannot** use `rgba(r g b a)` or `rgba(r g b / a)`
- A `transparent` string can also be used

## Example

```json
{
  "name": "Lavender Heaven",
  "description": "A theme made by Vodka",
  "authors": [
    {
      "name": "Vodka Martini",
      "id": "1068030255455015013"
    }
  ],
  "spec": 2,
  "semanticColors": {
    "HEADER_PRIMARY": ["#EFDFD7", "#E7D6CE", "#A07D6C"]
  },
  "rawColors": {
    "PRIMARY_500": "#9E8376"
  },
  "background": {
    "blur": 0.6,
    "url": "https://cdn.discordapp.com/attachments/1086985889286209586/1099189661995380897/82ef73f876a5ef467a8263b694e4f0b8.jpg",
    "alpha": 0.4
  }
}
```
