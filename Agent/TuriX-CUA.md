
# TuriX-CUA 

是一个让 AI 替你玩电脑的 AI 智能体。

它也是给 AI 装上眼睛和手，让它像人一样看着屏幕，动鼠标、敲键盘，帮你把活儿干了。

开源地址：https://github.com/TurixAI/TuriX-CUA


TuriX-CUA（Computer Use Agent）是一个基于 Python 的开源 Agent。它的核心逻辑非常暴力美学：

看（See）：每隔几秒截一张你屏幕的图。

想（Think）：把截图扔给多模态大模型，问它：“老铁，用户让我订机票，现在屏幕上这情况，我下一步该点哪？”

动（Act）：模型返回坐标，TuriX 控制你的鼠标移过去点击，或者在输入框里打字。

