# MazeMaker
Maze maker for Unity
![image](https://pbs.twimg.com/media/CzD_VT8VEAAiNuB.jpg
 "image")

# 特徴
Unity向け立体迷路自動生成プログラム

# 使用方法
1. 迷路を生成する範囲を設定する。
    1. 生成範囲となるオブジェクト(Cubeなど)を作成する。
    1. サイズは1x1x1より大きい任意サイズ。
    1. Mesh Rendererのチェックを外し不可視化すると良い。
1. 迷路生成の起点を設定する。
    1. 範囲のオブジェクト内側に、迷路の1単位になるGameObjectを生成する。
    1. サイズは1x1x1。傾いている場合、傾きに従って迷路を生成する。
    1. MazeMakerGrowInObjスクリプトをアタッチする。
1. 実行すると範囲オブジェクトの形状に沿って立体迷路を自動生成する。

# その他
- 任意のタイミングで迷路生成を実行したい場合、MazeMakerGrowInObjのGrow On Startチェックを外す。MazeMakerGrowInObjのGrow()を呼ぶと迷路生成が開始する。
- 生成範囲のオブジェクト以外は障害物として迂回して迷路を生成する。
- 任意形状のオブジェクトの内部に迷路を生成したい場合、[SA Collider Builder](https://www.assetstore.unity3d.com/jp/#!/content/15058)などで中が空洞のコライダを生成し、内部に迷路生成の起点を作成してください。
