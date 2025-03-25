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
