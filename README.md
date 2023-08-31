# easy-file-saver
Very Easily Save a File

# demo
https://danieljdufour.com/easy-file-saver/

# install
```bash
npm install easy-file-saver
```
or
```html
<script src="https://unpkg.com/easy-file-saver"></script>
```

# usage
```js
const saveFile = require("easy-file-saver");

const countries = [
    { name: "United States of America", abbreviation: "USA" },
    { name: "Canada", abbreviation: "CA" },
    { name: "Mexico", abbreviation: "MX" }
];
saveFile({ data: countries, debug: true, filename: "countries.csv" });
saveFile({ data: countries, debug: true, filename: "countries.tsv" });
saveFile({ data: countries, debug: true, filename: "countries.json" });
saveFile({ data: countries.map(c => `${c.name} (${c.abbreviation})`).join("\n"), debug: true, filename: "countries.txt" });
```

# features
saveFile supports the following conversions:
| data source      | output formats |
| ---------------- | -------------- |
| ArrayBuffer      | .csv, .jpg, .json, .html, .pdf, .png, .tsv, .txt, .webp |
| Array of Arrays  | .csv, .json, .tsv     |
| Array of Objects | .csv, .json, .tsv     |
| Blob             | .csv, .jpg, .json, .html, .png, .tsv, .txt, .webp |
| Canvas           | .jpg, .png, .webp |
| Data URL         | .csv, .jpg, .json, .html, .png, .tsv, .txt, .webp |
| File             | .csv, .jpg, .json, .html, .png, .tsv, .txt, .webp |
| HTML Element     | .html  |
| Image | .jpg, .png, .webp |
| Object           | .json  |
| String           | .html, .js, .py, .txt |
| Uint8Array       | .csv, .jpg, .json, .html, .pdf, .png, .tsv, .txt, .webp |

# any formats missing?
Post an issue at https://github.com/DanielJDufour/easy-file-saver or submit a Pull Request!
