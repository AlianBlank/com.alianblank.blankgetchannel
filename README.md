
# Unity 分发ios 和android 渠道号获取

该库主要服务于 `https://github.com/AlianBlank/GameFrameX` 作为子库使用。


# 使用方式(三种方式)
1. 直接在 `manifest.json` 文件中的`dependencies` 下添加以下内容
   ```json
      {"com.alianblank.blankgetchannel": "https://github.com/AlianBlank/com.alianblank.blankgetchannel.git"}
    ```
2. 在Unity 的`Packages Manager` 中使用`Git URL` 的方式添加库,地址为：https://github.com/AlianBlank/com.alianblank.blankgetchannel.git

3. 直接下载仓库放置到Unity 项目的`Packages` 目录下。会自动加载识别

# 改动功能

1. 增加`link.xml` 防止代码被裁剪

# Docs

> [文档说明在这里](https://blog.alianhome.com/BlankGetChannel)

# Example

```csharp

    using UnityEngine;

    public class BlankGetChannelExample : MonoBehaviour
    {
        private string value;
        void OnGUI()
        {
            GUILayout.Label(value);
            if (GUILayout.Button("GET", GUILayout.Width(200), GUILayout.Height(100)))
            {
                value = BlankGetChannel.GetChannelName("channel");
            }
        }
    }
```
