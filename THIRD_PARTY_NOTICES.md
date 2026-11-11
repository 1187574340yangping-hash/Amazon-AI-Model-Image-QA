# 第三方组件与许可声明

本仓库 `亚马逊AI模特图片检测工具/` 目录分发的是 **PyInstaller onedir** 构建产物。其中 `_internal/` 包含下列第三方运行时库与模型文件。它们的所有权和许可归各自权利人所有，本仓库仅作再分发，未修改其代码。

本项目的文档与项目自有脚本采用 [MIT](LICENSE) 许可；**MIT 不覆盖下列第三方二进制**。

## 运行时 / 依赖库

| 组件 | 用途 | 许可（以官方发布为准） |
|---|---|---|
| Python 3.13 (`python313.dll`) | 运行时 | PSF License |
| PySide6 / Qt 6 | 图形界面、信号槽、工作线程 | LGPLv3 / GPLv3（Qt 双重许可） |
| OpenCV (`cv2.pyd`, `opencv_videoio_ffmpeg*.dll`) | 图像读写、颜色空间、DNN 降级检测 | Apache-2.0；随附 FFmpeg 组件的许可取决于构建配置（LGPL/GPL） |
| ONNX Runtime (`onnxruntime*.dll`, `*_state.pyd`) | ONNX 模型推理 | MIT |
| NumPy + `libscipy_openblas64_*.dll` | 数组计算 | BSD-3-Clause；OpenBLAS 为 BSD-3-Clause |
| Pillow | 图像格式支持 | HPND / MIT-CMU |
| openpyxl | Excel 报告导出 | MIT |
| `libcrypto-3-x64.dll` / `libssl-3-x64.dll` | OpenSSL | Apache-2.0 (OpenSSL 3.x) |
| PyInstaller bootloader | 启动器 | GPLv2 with bootloader exception |

## ONNX 模型

| 模型 | 用途 | 来源 / 许可 |
|---|---|---|
| `person_det_mediapipe.onnx` | 人体检测 | 基于 Google MediaPipe 转换，Apache-2.0 / 对应模型许可 |
| `pphumanseg.onnx` | 人体分割 | PaddleSeg / PP-HumanSeg，Apache-2.0 |
| `yunet_face.onnx` | 人脸检测 | OpenCV Zoo YuNet，Apache-2.0 / OpenCV 许可 |

## 再分发说明

- 上述组件以**未修改的二进制形式**随程序提供，目的是让程序解压即可离线运行。
- 若你需要把这些组件用于自己的产品，请自行核对对应版本的官方许可文本与动态链接 / 源码提供等义务（尤其是 Qt 的 LGPL 与 FFmpeg 的 GPL 构建选项）。
- 若权利人对再分发有异议，请联系仓库维护者，我们会及时移除相关文件并改为下载指引。

## 商标

Amazon、亚马逊及 `contains-synthetic-performer` 相关规范属各自权利人。本项目是独立的辅助检查工具，与亚马逊官方无关联、无背书关系。合规口径请以卖家平台最新公告为准。
