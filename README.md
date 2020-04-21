# debian-setup-for-sic

debian setup for senior in college

# Debian Download

[Unofficial non-free images including firmware packages](http://cdimage.debian.org/cdimage/unofficial/non-free/cd-including-firmware/)からディスクイメージをダウンロードする(※ 例えば[これ](http://cdimage.debian.org/cdimage/unofficial/non-free/cd-including-firmware/10.3.0+nonfree/amd64/iso-dvd/firmware-10.3.0-amd64-DVD-1.iso))

# VirtualBox

1. [このページ](https://www.virtualbox.org/wiki/Downloads)から自分の OS にあったパッケージをダウンロードする

2. ダウンロードしたファイルを実行し、VirtualBox をインストールする

3. 「新規」をクリックする

4. 以下の通りに入力する
   ```
   名前: 任意()
   タイプ: Linux
   バージョン: Debian (64-bit)
   ```

5. メモリーサイズを選択する
   
6. 「仮想ハードディスクを作成する」を選択し、「作成」をクリックする

7. 「VDI (VirtualBox Disk Image)」を選択する

8. 「可変サイズ」を選択する

9. ファイルデータの上限を指定する

10. ホーム画面に戻り、上記で作成した仮想マシンの「設定」をクリックする

11. ストレージ→コントローラー:IDE→空→属性 内のディスクのマークをクリックする. 「仮想光学ディスクの選択/作成」をクリックして、上記でダウンロードした iso ファイルを選択する

12. ホーム画面に戻り、上記で作成した仮想マシンの「起動」をクリックすると Debian が起動する(はず)

## Guest Additions
1. 以下のコマンドを実行する
   ```shell
   sudo apt update
   sudo apt install gcc make perl linux-headers-$(uname -r)
   ```
   
2. VirtualBox の 「デバイス」→「Guest Additions CD イメージの挿入」をクリックする

3. 「実行する」を選択し、パスワードを入力する

4. 「Press Return to close this window...」と表示されたら、Enter を押す

## 参考
- [VirtualBox](https://www.virtualbox.org/)

# Debian Installation

## 参考
- https://github.com/lsnl/startup
- https://github.com/iPolyomino/debian-setup
- https://github.com/yukiue/debian-setup
