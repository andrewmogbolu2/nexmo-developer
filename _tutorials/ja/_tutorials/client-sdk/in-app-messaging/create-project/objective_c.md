---
title:  Xcodeプロジェクトとワークスペース
description:  このステップでは、Xcodeプロジェクトを作成し、iOSクライアントSDKライブラリを追加します。
---------------------------------------------------------------------------------------------

Xcodeプロジェクトとワークスペース
===================

次に作成するXcodeプロジェクト内で、iOSクライアントSDKライブラリを使用します。

Xcodeプロジェクトを作成する
----------------

* Xcodeを開き、メニューから `File`＞`New`＞`Project...`を選択します。

* アプリケーションタイプで`Single View App`を選択し、`Next`をクリックします。

* `AppToAppChat`の`Product Name`タイプで、関連する`Team`と`Organisation Identifier`を選択します。

* `Language`のユーザー`Objective-C`および`User Interface`の`Storyboard`。`Next`をクリックします。

* プロジェクトフォルダを配置する場所として、`Desktop`を選択します。別の場所を選択することもできますが、すぐに`Terminal`から移動する必要があるため、覚えておいてください。

* これで、新しいXcodeプロジェクトが作成されます。

**続行する前に、作成したばかりの新しいプロジェクトを閉じてください。** 

iOSクライアント SDK ライブラリを[CocoaPods](https://cocoapods.org/)経由でプロジェクトに追加します。

CocoaPodsをインストールする
------------------

* `Terminal`アプリを開き、入力してプロジェクトフォルダに移動します：

```shell
cd ~/Desktop/AppToAppChat
```

* まだインストールしていない場合、お使いのシステムにCocoaPodsをインストールしてください：

```shell
sudo gem install cocoapods
```

注：CocoaPodsは、macOS上でデフォルトで利用可能な、Rubyで構築されています。

* プロジェクトのPodfileを作成します：

```shell
pod init
```

iOSクライアントSDKを追加する
-----------------

* Vonage iOSクライアントSDKをPodfileに追加します。これを行うには、`Xcode`で開きましょう：

```shell
open -a Xcode Podfile
```

* 以下に示すように、Podfileを更新します：
````
# Uncomment the next line to define a global platform for your project
# platform :ios, '9.0'

target 'AppToAppChat' do
  # Comment the next line if you don't want to use dynamic frameworks
  use_frameworks!

  # Pods for AppToAppChat
  pod 'NexmoClient'
  
end
````
* ライブラリをインストールします：

```shell
pod install
```

ライブラリの最新バージョンがプロジェクトに追加されます：
````
Analyzing dependencies
Downloading dependencies
Installing NexmoClient (2.2.1)
Generating Pods project
Integrating client project

[!] Please close any current Xcode sessions and use `AppToAppChat.xcworkspace` for this project from now on.
Pod installation complete! There is 1 dependency from the Podfile and 1 total pod installed.

[!] Automatically assigning platform `iOS` with version `13.5` on target `AppToAppChat` because no platform was specified. Please specify a platform for this target in your Podfile. See `https://guides.cocoapods.org/syntax/podfile.html#platform`.
````
ワークスペースを開く

---

上記の出力で述べたように、今後は最初のプロジェクトではなく、`AppToAppChat.xcworkspace`を使用してください。このファイルを開くには、ターミナルに次のように入力します：

```shell
open AppToAppChat.xcworkspace
```

