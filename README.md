# MagnificationAPI_Control
PowerShellからMagnificationAPIで拡大鏡を制御するスクリプトです。    
  - 本体はps1ファイルです。.vbsはコンソールを立ち上げずに実行するためのものです。  
  - 名前付きパイプ経由で終了シグナルを受け取ると拡大状態が解除され縮小されます。  
  - **zoomout.ps1を実行するかプロセスを止めるか再起動しないと元に戻りません。**

#### 2024/01/06
VBScript廃止予告に伴いvbsを使用しないでコンソール画面を立ち上げずに実行する方法を追記しました。

### For beatmania IIDX INFINITAS
* JoyToKeyでE3/E4をvbsファイル実行 又は "run-hidden.exe + スクリプト実行" に割り当てることによって演奏レーンに合わせて拡大縮小できます。
  - この他にもファンクションキーやWindowsキーに絡むショートカットキーが殆どほとんど使えないという制約を回避して実行する方法が存在し、尚且別窓が立ち上がらなければ好きなタイミングで拡大縮小ができると思います。
  - [参考](https://note.3naly.xyz/view.php?id=00003)
* 2P側の場合はMagSetFullscreenTransform関数の2番目の引数を書き換えてください。
  - 1.5,0,211 --> 1.5,640,211
* 拡大した状態でINFINITASを起動してください。
  - "Now Loading..." で拡大していないと裏で流れている曲とキー音がズレます。
  - "Now Loading..." の後は一旦縮小したり演奏前に拡大するなど任意のタイミングで操作して問題ないです。
* 120FPS環境の場合は拡大しても120FPSのままプレーできます。
  - ASUS VG258Q(1280x720)で確認

### History
* 2023/02/16
  - 多重起動しないように修正しました。
* 2024/01/06
  - VBScriptが将来のWindowsリリースで削除すると予告がありました。  
  vbsの代わりに[run-hidden](https://github.com/stax76/run-hidden) (stax76様作)で拡大/縮小の制御を推奨します。
* 2024/03/14
  - FHDのアップデートに対応しました。

### 注意
このスクリプトを使用することによって生じる問題等の責任を一切負いません

