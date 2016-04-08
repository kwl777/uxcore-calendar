# uxcore-calendar

---

## TL;DR

transfer ui component for react

#### setup develop environment

```sh
$ git clone https://github.com/uxcore/uxcore-calendar
$ cd uxcore-calendar
$ npm install
$ gulp server
```

## Usage

```js
var Calendar = require('uxcore-calendar');
var MonthCalendar = Calendar.MonthCalendar;
var YearCalendar = Calendar.YearCalendar;
React.render(
  (<Calendar />),
  document.getElementById('target')
);
```

### demo
http://uxcore.github.io/uxcore/components/calendar/

## API
- onSelect(date, formatDateString)
    - date `date`
    - formatDateString `string`

### props

|参数|类型|默认值|说明|
|---|----|---|------|
|value|日期|string|无|
|defaultValue|日期|string|无|
|placeholder|placeholder文案|string|请选择日期|
|format|展示的日期格式|string|'yyyy-MM-dd'|
|locale|`en-us` 或`zh-cn`|string|`zh-cn`|
|disabledDate|日期|function|无|
|onSelect|日期|function|无|
|showTime|日期|boolean|false|
|disabled|日期|boolean|false|

#### MonthCalendar

|参数|类型|默认值|说明|
|---|----|---|------|
|value|日期|string|无|
|defaultValue|日期|string|无|
|placeholder|placeholder文案|string|请选择日期|
|format|展示的日期格式|string|'yyyy-MM'|
|locale|`en-us` 或`zh-cn`|string|`zh-cn`|
|onSelect|日期|function|无|
|disabled|日期|boolean|false|

#### YearCalendar

|参数|类型|默认值|说明|
|---|----|---|------|
|value|日期|string|无|
|defaultValue|日期|string|无|
|placeholder|placeholder文案|string|请选择日期|
|format|展示的日期格式|string|'yyyy'|
|locale|`en-us` 或`zh-cn`|string|`zh-cn`|
|onSelect|日期|function|无|
|disabled|日期|boolean|false|

#### util

> 一些辅助函数，用于某些套餐化定制

* Calendar.util.generateContentRender(code, locale): 用于在日历上标注非常规的休假、上班以及日程。
    * code should be an object like this {'xxxx-xx-xx': ['work/leave/schedule']}
    * locale should be `zh-cn` or `en-us`