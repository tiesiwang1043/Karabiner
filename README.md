# Karabiner
这是我的独家快捷键 mac 达芬奇 FCPX  ...
这里是我多年积攒的具有妙用的玩意,希望可以让你成为一个优秀牛马.
This is the machine translation.
Karabiner
These are my exclusive shortcuts for Mac's DaVinci Resolve and Final Cut Pro X...
These are the useful things I've accumulated over the years. I hope they can help you become an outstanding professional in this regard.
从这里开始就是标准代码:
长安退格键,执行command+backspace 这样大家就可以删除了
{
    "manipulators": [
        {
            "description": "⌘删除：长按 Delete 执行 Command+Delete（删除光标后内容或文件）",
            "from": {
                "key_code": "delete_or_backspace",
                "modifiers": { "optional": ["any"] }
            },
            "parameters": { "basic.to_if_alone_timeout_milliseconds": 300 },
            "to_if_alone": [{ "key_code": "delete_or_backspace" }],
            "to_if_held_down": [
                {
                    "key_code": "delete_or_backspace",
                    "modifiers": ["left_command"]
                }
            ],
            "type": "basic"
        }
    ]
}

2.这是第二个有意思的快捷键 它主要是满足我使用AE的需求
目前需要修改,之后我会再次修改发布到这里
3·这是第三个有意思的,键盘修改.这个需要键盘上有旋钮.比如可以调节音量的.
我这个功能是 把旋钮,映射成多功能 可以调节音量 可以调节 亮度 只需要按住不同功能的修饰肩即可获得这些功能
{
    "manipulators": [
        {
            "description": "多功能旋钮改造",
            "from": {
                "key_code": "comma",
                "modifiers": { "mandatory": ["option"] }
            },
            "to": [{ "key_code": "volume_decrement" }],
            "type": "basic"
        },
        {
            "description": "Fn+. → 音量增大",
            "from": {
                "key_code": "period",
                "modifiers": { "mandatory": ["option"] }
            },
            "to": [{ "key_code": "volume_increment" }],
            "type": "basic"
        },
        {
            "description": "Shift+, → 亮度降低",
            "from": {
                "key_code": "comma",
                "modifiers": { "mandatory": ["shift"] }
            },
            "to": [{ "consumer_key_code": "display_brightness_decrement" }],
            "type": "basic"
        },
        {
            "description": "Shift+. → 亮度升高",
            "from": {
                "key_code": "period",
                "modifiers": { "mandatory": ["shift"] }
            },
            "to": [{ "consumer_key_code": "display_brightness_increment" }],
            "type": "basic"
        }
    ],
    "title": "Fn/Shift组合键自定义映射"
}

这是第四个有意思的快捷键映射
