# Release Notes
This file records the **main** changes in *PyLf* library.

## in progress version
* __将依赖项由`pillow >= 4.3.0`改为`5.0.0 <= pillow < 6`__
* __将`font_size / 256`作为`template`中`font_size_sigma`、`word_spacing_sigma`和`line_spacing_sigma`参数的缺省值__
* __`template`添加新的参数`alpha_x`和`alpha_y`__
* __`handwrite`的返回值中图片的`mode`将由与`background`保持一致改为均为`RGB`__
* __废除参数`anti_aliasing`__
* __大幅提高性能，大幅减少内存占用__
* __将`line_spacing`的含义改为两临近行间的间隙（即上一行字的下端和下一行字的上端的距离）的大小（以像素为单位），并将
`font_size // 5`作为其缺省值__
* 完善文档

## v0.5.2 (2017-12-30)
* __将`0`作为`word_spacing`的缺省值__
* __修复当生成图片数超过`worker`时文字出现大范围重叠的漏洞__

## v0.5.1 (2017-12-14)
* fix #2

## v0.5.0 (2017-12-14)
* __改进算法使得参数`text`可为`iterable`__

## v0.4.0 (2017-12-5)
* Add `ValueError` raised by `handwrite` to prevent dead loop in some corner cases
* 完善文档
* __将黑色作为`template`的缺省颜色__
* __字体宽度从由`font_size`决定改为由每个字符自己的信息决定__
* __将`lambda c: False`作为`is_half_char`的缺省值__
* __将是否在常见非开头字符集中作为`is_end_char`的缺省值__