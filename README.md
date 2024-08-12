# Toggle Switch Example

## HTML

```html
<div class="switch-wrapper">
    <input id="option-1" type="radio" name="switch" checked>
    <input id="option-2" type="radio" name="switch">
    <label for="option-1">เดือน</label>
    <label for="option-2">ปี</label>
    <span class="highlighter"></span>
</div>
```

## CSS

```html
        .switch-wrapper {
            position: relative;
            display: inline-flex;
            border: 1px solid lightgrey;
            border-radius: 30px;
            background: #2c2c2c;
            align-items: center;
        }

        .switch-wrapper [type="radio"] {
            position: absolute;
            left: -9999px;
        }

        .switch-wrapper [type="radio"]:checked#option-1~label[for="option-1"],
        .switch-wrapper [type="radio"]:checked#option-2~label[for="option-2"] {
            color: black;
        }

        .switch-wrapper [type="radio"]:checked#option-1+label[for="option-2"]~.highlighter {
            transform: none;
        }

        .switch-wrapper [type="radio"]:checked#option-2+label[for="option-1"]~.highlighter {
            transform: translateX(100%);
        }

        .switch-wrapper label {
            font-size: 16px;
            z-index: 1;
            min-width: 60px;
            line-height: 32px;
            cursor: pointer;
            border-radius: 30px;
            text-align: center;
            transition: color 0.25s ease-in-out;
        }

        .switch-wrapper label:hover {
            background: rgba(0, 0, 0, 0.1);
        }

        .switch-wrapper .highlighter {
            position: absolute;
            top: 4px;
            left: 4px;
            width: calc(50% - 4px);
            height: calc(100% - 8px);
            border-radius: 30px;
            background: white;
            transition: transform 0.25s ease-in-out;
        }





