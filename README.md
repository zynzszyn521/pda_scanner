# PDA Scanner
  
[![License][license-image]][license-url] 
[![Pub](https://img.shields.io/pub/v/pda_scanner.svg?style=flat-square)](https://pub.dartlang.org/packages/pda_scanner)

A Flutter plugin ð  to scanning. Ready for PDA ð 

[github](https://github.com/leyan95/pda_scanner)

![pda_scanner.gif](https://upload-images.jianshu.io/upload_images/3646846-16ca17b573a765f2.gif?imageMogr2/auto-orient/strip%7CimageView2/2/w/320/format/webp)

## Installation

Add this to your package's pubspec.yaml file:

```
dependencies:
 pda_scanner: ^0.2.9
```

## Supported

-  [x] SEUIC(å°ç å¥)-PDA
-  [x] IData(çè¾¾èå)-PDA
-  [x] UROVO(ä¼åè®¯)-PDA
-  [x] HONEYWELL(éå°¼é¦å°)-PDA
-  [x] PL(æå)-PDA

## Usage
```dart
/// å¯¼å¥ä¾èµ
import 'package:pda_scanner/pda_source.dart';
import 'package:pda_scanner/pda_listener_mixin.dart';
import 'package:pda_scanner/pda_lifecycle_mixin.dart';

/// èªå¨ç®¡çpdaçå½å¨æ (èªå¨åå§ååèªå¨éæ¾)ï¼ä½¿ç¨PdaLifecycleMixinæ··å¥appæ ¹ç»ä»¶ç¶æã
/// å¦æéå°å¤æ··å¥çæåµè¯·æå¨è¿è¡çå½å¨æçåå§å `super.initPdaLifecycle()` å éæ¾ `super.disposePdaLifecycle()` 
class RootWidgetState extends State<RootWidget> with PdaLifecycleMixin<RootWidget> {
  @override
  Widget build(BuildContext context) {
    // TODO
  }
}

/// æ··å¥ PdaListenerMixin çå¬æ«ç äºä»¶
/// å¦æéå°å¤æ··å¥çæåµè¯·æå¨è¿è¡çå½å¨æçåå§å `super.registerPdaListener()` å éæ¾ `super.unRegisterPdaListener()` 
class PageAlphaState extends State<PageAlpha> with PdaListenerMixin<PageAlpha> {
  var _code;

  @override
  Widget build(BuildContext context) {
    return null;
  }

  @override
  void onEvent(Object event) {
      // TODO: implement onEvent
  }
  
    @override
  void onError(Object error) {
      // TODO: implement onError
  }
}
```

## Contribute

We would â¤ï¸ to see your contribution!

## License

Distributed under the MIT license. See ``LICENSE`` for more information.

## About

Created by Shusheng.

[license-image]: https://img.shields.io/badge/License-MIT-blue.svg
[license-url]: LICENSE
