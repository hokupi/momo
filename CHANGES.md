# 変更履歴

- UPDATE
    - 下位互換がある変更
- ADD
    - 下位互換がある追加
- CHANGE
    - 下位互換のない変更
- FIX
    - バグ修正

## develop

## 18.10.0

**18.10.0-rc4 から変更なし**

## 18.10.0-rc4

- [ADD] 4K の配信にに対応する
    - armv6, armv7 にも対応はしているが、現時点で Raspberry Pi で配信はマシンパワー不足のためできない

## 18.10.0-rc3

- [FIX] バージョン情報を MOMO_VERSION に指定したら momo のバイナリの --version も反映するようにする
- [CHANGE] --metadata の引数は JSON のみを指定できるようにする

## 18.10.0-rc2

- [CHANGE] libwebrtc が 4K に対応していないため解像度指定から 4K を削除する
    - 将来的に対応していく予定
    - https://github.com/shiguredo/momo/issues/21
- [FIX] P2P モードのサンプルで映像を有効にした場合、音声が正常に流れない問題を修正

## 18.10.0-rc1

- [UPDATE] ビルド時に `LDFLAGS += -s` 渡してバイナリサイズを圧縮する仕組みを追加
- [ADD] WebRTC が依存しているライブラリのライセンスを追加
- [ADD] Websocketpp が依存しているライブラリのライセンスを追加
- [FIX] P2P モードで画面を開いているときに終了するとセグフォが起きるのを修正

## 18.10.0-rc0

**初 リリース**

- Momo を Apache License 2.0 でオープンソース化
- libwebrtc M70 対応
- Ubuntu 18.04 x86_64 対応
    - Ubuntu 18.04 x86_64 向けのバイナリの提供
- Ubuntu 16.04 ARMv8 対応
    - Ubuntu 16.04 ARMv8 向けのバイナリの提供
    - PINE64 の Rock64 対応
- Raspberry Pi 3 B/B+ 対応
    - Raspberry Pi 3 B/B+ 向け ARMv7 バイナリの提供
    - Raspberry Pi 3 B/B+ 向け H.264 HWA 対応
- Raspberry Pi Zero W/WH 対応
    - Raspberry Pi Zero W/WH 向け ARMv6 バイナリの提供
    - Raspberry Pi Zero W/WH 向け H.264 HWA 対応
- 解像度指定オプション
    - QVGA、VGA、HD、FHD、4K
- フレームレート指定オプション
    - 1-60
- 優先オプション
    - この機能は実験的機能です
    - フレームレートか解像度のどちらを優先するか指定可能
- ビデオを利用しないオプション
- オーディオを利用しないオプション
- ビデオコーデック指定オプション
- オーディオコーデック指定オプション
- デーモン化オプション
    - Systemd の利用をおすすめします
- ログレベル
- P2P 機能
- WebRTC SFU Sora 18.04.12 対応
