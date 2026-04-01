# RotateLabelme
一个批量旋转 Labelme 标注数据的工具，能同时旋转图片和对应的 JSON 标注（多边形、矩形等），并保持标注与新图片的坐标对应。


默认逆时针旋转 90 度（通过更改 parser 参数来改变逆时针旋转的角度）。

> **注意**：只要你输出路径和原文件路径不同，就不会破坏原有数据。如果你不放心，可以先备份，再使用。

## 两种使用方式（选一即可）

### 方式一：直接运行脚本

将 `main()` 函数中 parser 的所有 default 参数配置完成后，直接运行脚本文件。

### 方式二：命令行调用

在命令行调用，引号内需要你填入相应的参数：

```bash
# 指定输入输出文件夹，逆时针旋转 180 度
python rotate_labelme.py \
  --img_dir "你的图片路径" \
  --json_dir "你的json文件路径" \
  --out_img_dir "输出图片路径" \
  --out_json_dir "输出json路径" \
  --angle 90
```



使用建议：

最好是旋转90度的整数倍，否则标签可能不会完全贴合。比如一个旋转45°的例子：

<img width="1526" height="1319" alt="image" src="https://github.com/user-attachments/assets/4494f7b7-829a-4fb6-9fa9-448a90f5b46a" />
