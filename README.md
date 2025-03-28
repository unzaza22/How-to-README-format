# How-to-README-format
วิธีการใช้งาน Github

## การสร้างตาราง(Creating a table)
#### Syntax:
```
| First Header  | Second Header |
| ------------- | ------------- |
| Content Cell  | Content Cell  |
| Content Cell  | Content Cell  |

| Command | Description |
| --- | --- |
| git status | List all new or modified files |
| git diff | Show file differences that haven't been staged |
```
#### Output:
| First Header  | Second Header |
| ------------- | ------------- |
| Content Cell  | Content Cell  |
| Content Cell  | Content Cell  |

| Command | Description |
| --- | --- |
| git status | List all new or modified files |
| git diff | Show file differences that haven't been staged |

## การรูปแบบในตาราง
#### Syntax:
```
| Command | Description |
| --- | --- |
| `git status` | List all *new or modified* files | // ทำให้ตัวอักษรเอียง
| `git diff` | Show file differences that **haven't been** staged | // ทำให้ตัวอักษรหน้า

| Left-aligned | Center-aligned | Right-aligned |
| :---         |     :---:      |          ---: | // จัดรูปแบบ ซ้าย กลาง ขวา
| git status   | git status     | git status    |
| git diff     | git diff       | git diff      |

| Name     | Character |
| ---      | ---       |
| Backtick | `         |
| Pipe     | \|        | // ยกเลิกสัญลักษณ์ markdown
```
#### Output:
| Command | Description |
| --- | --- |
| `git status` | List all *new or modified* files |
| `git diff` | Show file differences that **haven't been** staged |

| Left-aligned | Center-aligned | Right-aligned |
| :---         |     :---:      |          ---: |
| git status   | git status     | git status    |
| git diff     | git diff       | git diff      |

| Name     | Character |
| ---      | ---       |
| Backtick | `         |
| Pipe     | \|        |

## การสร้างดรอปดาวแบบพับเก็บ(Creating a collapsed section)
#### Syntax:
````
<details> // สามารถใช้ <details open> ได้เพื่อเปิดพับไว้เลย

<summary>Tips for collapsed sections</summary>

### You can add a header

You can add text within a collapsed section.

You can add an image or a code block, too.

```python
   print("Hello World")
```

</details>
````
#### Output:
<details>

<summary>Tips for collapsed sections</summary>

### You can add a header

You can add text within a collapsed section.

You can add an image or a code block, too.

```python
   print("Hello World")
```

</details>

## การสร้างบล็อค(Blocks)
#### Syntax:
`````
 ```
function test() {
  console.log("notice the blank line before this function?");
}
```

````
```
Look! You can see my backticks.
```
````
`````
#### Output:
 ```
function test() {
  console.log("notice the blank line before this function?");
}
```

````
```
Look! You can see my backticks.
```
````

## ไฮไลท์โค้ด(Syntax highlighting)
#### Syntax:
````
```python
markdown = "Hello World!"
print(markdown)
```
````
#### Output:
```python
markdown = "Hello World!"
print(markdown)
```

## สร้างไดอะแกรม(Creating Mermaid diagrams)
#### Syntax:
````
Here is a simple flow chart:

```mermaid
graph TD;
    A-->B;
    A-->C;
    B-->D;
    C-->D;
```
// สามารถใช้เพื่อเช็คเวอร์ชั่นได้
```mermaid
  info
```
````
#### Output:
Here is a simple flow chart:

```mermaid
graph TD;
    A-->B;
    A-->C;
    B-->D;
    C-->D;
```

```mermaid
  info
```

[Mermaid docs](https://mermaid.js.org/)

## สร้างแผนที่(Creating GeoJSON and TopoJSON maps)
#### Using GeoJSON
#### Syntax:
````
```geojson
{
  "type": "FeatureCollection",
  "features": [
    {
      "type": "Feature",
      "id": 1,
      "properties": {
        "ID": 0
      },
      "geometry": {
        "type": "Polygon",
        "coordinates": [
          [
              [-90,35],
              [-90,30],
              [-85,30],
              [-85,35],
              [-90,35]
          ]
        ]
      }
    }
  ]
}
```
````
#### Output:
```geojson
{
  "type": "FeatureCollection",
  "features": [
    {
      "type": "Feature",
      "id": 1,
      "properties": {
        "ID": 0
      },
      "geometry": {
        "type": "Polygon",
        "coordinates": [
          [
              [-90,35],
              [-90,30],
              [-85,30],
              [-85,35],
              [-90,35]
          ]
        ]
      }
    }
  ]
}
```
[GeoJSON](https://geojson.io/#map=2/0/20)

#### Using TopoJSON
#### Syntax:
````
```topojson
{
  "type": "Topology",
  "transform": {
    "scale": [0.0005000500050005, 0.00010001000100010001],
    "translate": [100, 0]
  },
  "objects": {
    "example": {
      "type": "GeometryCollection",
      "geometries": [
        {
          "type": "Point",
          "properties": {"prop0": "value0"},
          "coordinates": [4000, 5000]
        },
        {
          "type": "LineString",
          "properties": {"prop0": "value0", "prop1": 0},
          "arcs": [0]
        },
        {
          "type": "Polygon",
          "properties": {"prop0": "value0",
            "prop1": {"this": "that"}
          },
          "arcs": [[1]]
        }
      ]
    }
  },
  "arcs": [[[4000, 0], [1999, 9999], [2000, -9999], [2000, 9999]],[[0, 0], [0, 9999], [2000, 0], [0, -9999], [-2000, 0]]]
}
```
````
#### Output:
```topojson
{
  "type": "Topology",
  "transform": {
    "scale": [0.0005000500050005, 0.00010001000100010001],
    "translate": [100, 0]
  },
  "objects": {
    "example": {
      "type": "GeometryCollection",
      "geometries": [
        {
          "type": "Point",
          "properties": {"prop0": "value0"},
          "coordinates": [4000, 5000]
        },
        {
          "type": "LineString",
          "properties": {"prop0": "value0", "prop1": 0},
          "arcs": [0]
        },
        {
          "type": "Polygon",
          "properties": {"prop0": "value0",
            "prop1": {"this": "that"}
          },
          "arcs": [[1]]
        }
      ]
    }
  },
  "arcs": [[[4000, 0], [1999, 9999], [2000, -9999], [2000, 9999]],[[0, 0], [0, 9999], [2000, 0], [0, -9999], [-2000, 0]]]
}
```

## สร้าง 3D โมเดล(Creating STL 3D models)
#### Syntax:
````
```stl
solid cube_corner
  facet normal 0.0 -1.0 0.0
    outer loop
      vertex 0.0 0.0 0.0
      vertex 1.0 0.0 0.0
      vertex 0.0 0.0 1.0
    endloop
  endfacet
  facet normal 0.0 0.0 -1.0
    outer loop
      vertex 0.0 0.0 0.0
      vertex 0.0 1.0 0.0
      vertex 1.0 0.0 0.0
    endloop
  endfacet
  facet normal -1.0 0.0 0.0
    outer loop
      vertex 0.0 0.0 0.0
      vertex 0.0 0.0 1.0
      vertex 0.0 1.0 0.0
    endloop
  endfacet
  facet normal 0.577 0.577 0.577
    outer loop
      vertex 1.0 0.0 0.0
      vertex 0.0 1.0 0.0
      vertex 0.0 0.0 1.0
    endloop
  endfacet
endsolid
```
````
#### Output:
```stl
solid cube_corner
  facet normal 0.0 -1.0 0.0
    outer loop
      vertex 0.0 0.0 0.0
      vertex 1.0 0.0 0.0
      vertex 0.0 0.0 1.0
    endloop
  endfacet
  facet normal 0.0 0.0 -1.0
    outer loop
      vertex 0.0 0.0 0.0
      vertex 0.0 1.0 0.0
      vertex 1.0 0.0 0.0
    endloop
  endfacet
  facet normal -1.0 0.0 0.0
    outer loop
      vertex 0.0 0.0 0.0
      vertex 0.0 0.0 1.0
      vertex 0.0 1.0 0.0
    endloop
  endfacet
  facet normal 0.577 0.577 0.577
    outer loop
      vertex 1.0 0.0 0.0
      vertex 0.0 1.0 0.0
      vertex 0.0 0.0 1.0
    endloop
  endfacet
endsolid
```

## การใช้งานสัญลักษณ์ทางคณิตศาสตร์(Writing mathenatilcal expressions)
#### Syntax:
```
This sentence uses `$` delimiters to show math inline: $\sqrt{3x-1}+(1+x)^2$ // $\ สมการ
This sentence uses $\` and \`$ delimiters to show math inline: $`\sqrt{3x-1}+(1+x)^2`$ // $`สมการ`$
```
#### Output:
This sentence uses `$` delimiters to show math inline: $\sqrt{3x-1}+(1+x)^2$<br />
This sentence uses $\` and \`$ delimiters to show math inline: $`\sqrt{3x-1}+(1+x)^2`$

## สร้างคณิตศาสตร์ในรูปแบบบล็อค(Writing expressions as blocks)
#### Syntax:
````
**The Cauchy-Schwarz Inequality**\
$$\left( \sum_{k=1}^n a_k b_k \right)^2 \leq \left( \sum_{k=1}^n a_k^2 \right) \left( \sum_{k=1}^n b_k^2 \right)$$ // ใช้ $$ แล้วปิดด้วย $$

**The Cauchy-Schwarz Inequality**

```math
\left( \sum_{k=1}^n a_k b_k \right)^2 \leq \left( \sum_{k=1}^n a_k^2 \right) \left( \sum_{k=1}^n b_k^2 \right) //หรือใช้ ```math ปิดด้วย ```
```
````
#### Output:
**The Cauchy-Schwarz Inequality**\
$$\left( \sum_{k=1}^n a_k b_k \right)^2 \leq \left( \sum_{k=1}^n a_k^2 \right) \left( \sum_{k=1}^n b_k^2 \right)$$

**The Cauchy-Schwarz Inequality**

```math
\left( \sum_{k=1}^n a_k b_k \right)^2 \leq \left( \sum_{k=1}^n a_k^2 \right) \left( \sum_{k=1}^n b_k^2 \right)
```

## วิธีใช้สัญลักษณ์ $ (Writing dollar signs in line with and within mathematical expressions)
#### Syntax:
```
This expression uses `\$` to display a dollar sign: $`\sqrt{\$4}`$

To split <span>$</span>100 in half, we calculate $100/2$

// จะใช้ \$ หรือ <span>$</span> ก็ได้
```
#### Output:
This expression uses `\$` to display a dollar sign: $`\sqrt{\$4}`$<br />
To split <span>$</span>100 in half, we calculate $100/2$

## URLs
#### Syntax:
```
Visit https://github.com
```
#### Output:
Visit https://github.com

## สร้าง Checkbox(Creating task list)
#### Syntax:
```
- [x] #739
- [ ] https://github.com/octo-org/octo-repo/issues/740
- [ ] Add delight to the experience when all tasks are complete :tada:
```
#### Output:
- [x] #739
- [ ] https://github.com/octo-org/octo-repo/issues/740
- [ ] Add delight to the experience when all tasks are complete :tada:
