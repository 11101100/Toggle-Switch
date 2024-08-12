# Toggle-Switch

<style>
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

    .switch-wrapper [type="radio"]:checked#monthly~label[for="monthly"],
    .switch-wrapper [type="radio"]:checked#yearly~label[for="yearly"] {
        color: black;
    }

    .switch-wrapper [type="radio"]:checked#monthly~label[for="monthly"]:hover,
    .switch-wrapper [type="radio"]:checked#yearly~label[for="yearly"]:hover {
        background: transparent;
    }

    .switch-wrapper [type="radio"]:checked#monthly+label[for="yearly"]~.highlighter {
        transform: none;
    }

    .switch-wrapper [type="radio"]:checked#yearly+label[for="monthly"]~.highlighter {
        transform: translateX(100%);
    }

    .switch-wrapper label {
        font-size: 16px;
        color:white;
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
</style>    

<div class="switch-wrapper">
    <input id="monthly" type="radio" name="switch" checked>
    <input id="yearly" type="radio" name="switch">
    <label for="monthly">เดือน</label>
    <label for="yearly">ปี</label>
    <span class="highlighter"></span>
</div>

# Toggle Switch Example

นี่คือตัวอย่างการสร้างปุ่มสลับ (Toggle Switch) สำหรับการเลือก "เดือน" และ "ปี":

```html
<style>
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

    .switch-wrapper [type="radio"]:checked#monthly~label[for="monthly"],
    .switch-wrapper [type="radio"]:checked#yearly~label[for="yearly"] {
        color: black;
    }

    .switch-wrapper [type="radio"]:checked#monthly~label[for="monthly"]:hover,
    .switch-wrapper [type="radio"]:checked#yearly~label[for="yearly"]:hover {
        background: transparent;
    }

    .switch-wrapper [type="radio"]:checked#monthly+label[for="yearly"]~.highlighter {
        transform: none;
    }

    .switch-wrapper [type="radio"]:checked#yearly+label[for="monthly"]~.highlighter {
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
</style>    

<div class="switch-wrapper">
    <input id="monthly" type="radio" name="switch" checked>
    <input id="yearly" type="radio" name="switch">
    <label for="monthly">เดือน</label>
    <label for="yearly">ปี</label>
    <span class="highlighter"></span>
</div>
