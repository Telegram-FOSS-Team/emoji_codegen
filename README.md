### emoji_codegen

`cd src && make`
`./emoji_codegen ../emoji_autocomplete.json`

This generates `emoji_suggestions_data.{h,cpp}` which is used by Telegram-Android. The other set of files `emoji_suggestions.{h,cpp}` comes from here: `https://github.com/telegramdesktop/tdesktop/tree/dev/Telegram/ThirdParty/emoji_suggestions`
