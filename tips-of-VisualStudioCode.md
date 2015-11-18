#VisualStudio Codeで.ejsにhtmlシンタックスハイライトを当てる
##シンタックスコードなどの拡張コードの保存先
* Windows環境
 - %USERPROFILE%.vscode\extensions
* Mac/Linux環境
 - $HOME/.vscode/extensions

##シンタックスファイルを探す
* (http://colorsublime.com)

## ejsファイルのシンタックスファイル
* (https://github.com/samholmes/EJS.tmLanguage)

##準備
* 上記urlなどでファイルをダウンロード
* yoを使ってジェネレート
 - yo と code が必要なので いれる`npm install -g yo generator-code`
 - **You can see available generators with npm search yeoman-generator and then install them with npm install [name].**とかって出てきたら、`yo doctor`して確認
 - `yo code`でジェネレータ起動
 - ダウンロードしてきたファイルのパス(やurl)などを指定して完了後、出来上がったファイルを%USERPROFILE%.vscode\extensionsに移してvisualStudio Code再起動

