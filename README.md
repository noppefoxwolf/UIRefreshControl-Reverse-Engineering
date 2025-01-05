# UIRefreshControl

## View Hierarchy

```
UIRefreshControl
 _UIRefreshControlModernContentView
  UIView
   _UIRefreshControlModernReplicatorView
    _UIRefreshControlSeedView
  UILabel
```

## _style

```
refreshControl.style = 0 // automatic
refreshControl.style = 1 // legacy?
refreshControl.style = 2 // modern
```

## refreshControlState

|rawValue||appliedInsets|
|---|---|---|
|0|idle|UIEdgeInsets: {0, 0, 0, 0}|
|1|pulling|UIEdgeInsets: {0, 0, 0, 0}|
|3|refreshing|UIEdgeInsets: {60, 0, 0, 0}|
|6|returning|UIEdgeInsets: {0, 0, 0, 0}|

## values

|property|value|
|---|---|
|_snappingHeight|150.3301056338028|
|_refreshControlHeight|60.0|
|_areInsetsBeingApplied|true/false|
|_scrollViewHeight|scrollView.bounds.height|

## Runtime headers

https://github.com/nst/iOS-Runtime-Headers/blob/master/PrivateFrameworks/UIKitCore.framework/UIRefreshControl.h

```
Optional(Swift.Unmanaged<Swift.AnyObject>(_value: <UIRefreshControl: 0x102106a00>:
in UIRefreshControl:
	Class Methods:
		+ (id) fallback_debugHierarchyPropertyDescriptions; (0x248e86028)
		+ (id) fallback_debugHierarchyValueForPropertyWithName:(id)arg1 onObject:(id)arg2 outOptions:(id*)arg3 outError:(id*)arg4; (0x248e86118)
		+ (BOOL) _allowsUnsupportedMacIdiomBehavior; (0x185f34d38)
		+ (Class) _contentViewClassForStyle:(long)arg1; (0x18541d7f4)
		+ (id) _defaultColor; (0x18541d74c)
		+ (void) _setAllowsUnsupportedMacIdiomBehavior:(BOOL)arg1; (0x185f34d14)
	Properties:
		@property (readonly) unsigned long hash;
		@property (readonly) Class superclass;
		@property (readonly, copy) NSString* description;
		@property (readonly, copy) NSString* debugDescription;
		@property (readonly, nonatomic) long refreshControlState;  (@synthesize refreshControlState = _refreshControlState;)
		@property (readonly, nonatomic) long style;
		@property (readonly, nonatomic) double _refreshControlHeight;
		@property (readonly, nonatomic) double _snappingHeight;
		@property (readonly, nonatomic) double _visibleHeight;
		@property (readonly, nonatomic) BOOL _hostAdjustsContentOffset;
		@property (readonly, nonatomic) BOOL _areInsetsBeingApplied;
		@property (readonly, nonatomic, getter=_appliedInsets) struct UIEdgeInsets appliedInsets;
		@property (weak, nonatomic, getter=_host, setter=_setHost:) <_UIRefreshControlHosting>* _host;
		@property (readonly, nonatomic, getter=isRefreshing) BOOL refreshing;
		@property (retain, nonatomic) UIColor* tintColor;
		@property (retain, nonatomic) NSAttributedString* attributedTitle;
	Instance Methods:
		- (void) dealloc; (0x18541dbdc)
		- (id) description; (0x18541dc30)
		- (id) init; (0x100cef7d0)
		- (void) .cxx_destruct; (0x18541f5a8)
		- (void) encodeWithCoder:(id)arg1; (0x100cef7d8)
		- (id) initWithCoder:(id)arg1; (0x100cef7e0)
		- (void) _update; (0x18541eb44)
		- (id) attributedTitle; (0x100cef7e8)
		- (void) setAttributedTitle:(id)arg1; (0x100cef7f0)
		- (long) style; (0x100cef7f8)
		- (void) setBounds:(struct CGRect)arg1; (0x100cef800)
		- (id) _host; (0x18541f574)
		- (id) initWithFrame:(struct CGRect)arg1; (0x100cef808)
		- (void) setBackgroundColor:(id)arg1; (0x100cef810)
		- (void) setFrame:(struct CGRect)arg1; (0x100cef818)
		- (double) _snappingHeight; (0x18541e8f0)
		- (void) _setRefreshControlState:(long)arg1 notify:(BOOL)arg2; (0x18541f3d0)
		- (void) beginRefreshing; (0x100cef820)
		- (void) _addInsetHeight:(double)arg1; (0x18541ed30)
		- (void) _addInsets; (0x18541ece8)
		- (struct UIEdgeInsets) _appliedInsets; (0x18541e920)
		- (BOOL) _areInsetsBeingApplied; (0x18541e900)
		- (id) _attributedTitle; (0x18541e364)
		- (BOOL) _canTransitionFromState:(long)arg1 toState:(long)arg2; (0x18541f344)
		- (id) _contentView; (0x18541e144)
		- (unsigned long) _controlEventsForActionTriggered; (0x18541f548)
		- (void) _didScroll; (0x18541eac8)
		- (void) _endRefreshingAnimated:(BOOL)arg1; (0x18541efc8)
		- (BOOL) _hostAdjustsContentOffset; (0x18541f550)
		- (double) _impactIntensityForVelocity:(double)arg1; (0x18541eb0c)
		- (BOOL) _isApplyingInsets; (0x18541e910)
		- (struct CGPoint) _originForContentOffset:(struct CGPoint)arg1; (0x18541e938)
		- (void) _populateArchivedSubviews:(id)arg1; (0x18541da7c)
		- (long) _recomputeNewState; (0x18541e454)
		- (double) _refreshControlHeight; (0x18541e208)
		- (void) _removeInsetHeight:(double)arg1; (0x18541edb0)
		- (void) _removeInsets; (0x18541ed0c)
		- (void) _resizeToFitContents; (0x18541e3b4)
		- (id) _scrollView; (0x18541f2ec)
		- (double) _scrollViewHeight; (0x18541f2fc)
		- (void) _setAttributedTitle:(id)arg1; (0x18541e314)
		- (void) _setHost:(id)arg1; (0x18541f584)
		- (void) _setTintColor:(id)arg1; (0x18541e218)
		- (void) _setVisibleHeight:(double)arg1; (0x18541e76c)
		- (double) _stiffnessForVelocity:(double)arg1; (0x18541eacc)
		- (id) _tintColor; (0x18541e298)
		- (void) _updateConcealingMask; (0x18541f17c)
		- (void) _updateHiddenStateIfNeeded; (0x18541e6fc)
		- (void) _updateSnappingHeight; (0x18541e7d0)
		- (double) _visibleHeight; (0x18541e444)
		- (double) _visibleHeightForContentOffset:(struct CGPoint)arg1 origin:(struct CGPoint)arg2; (0x18541ea24)
		- (void) didMoveToSuperview; (0x100cef828)
		- (void) endRefreshing; (0x100cef830)
		- (id) initWithStyle:(long)arg1; (0x100cef838)
		- (BOOL) isRefreshing; (0x100cef840)
		- (long) refreshControlState; (0x100cef848)
		- (double) revealedFraction; (0x100cef850)
		- (void) setRefreshControlState:(long)arg1; (0x100cef858)
		- (void) setTintColor:(id)arg1; (0x100cef860)
		- (struct CGSize) sizeThatFits:(struct CGSize)arg1; (0x100cef868)
		- (void) sizeToFit; (0x100cef870)
		- (id) tintColor; (0x100cef878)
```

## Stack traces

### init

```
UIKitCore`-[UIRefreshControl init]:
->  0x18541dbd4 <+0>: mov    w2, #0x2                  ; =2 
    0x18541dbd8 <+4>: b      0x186952820               ; objc_msgSend$initWithStyle:
```

### initWithStyle

```
UIKitCore`-[UIRefreshControl initWithStyle:]:
->  0x18541dae4 <+0>:   sub    sp, sp, #0x30
    0x18541dae8 <+4>:   stp    x20, x19, [sp, #0x10]
    0x18541daec <+8>:   stp    x29, x30, [sp, #0x20]
    0x18541daf0 <+12>:  add    x29, sp, #0x20
    0x18541daf4 <+16>:  mov    x19, x2
    0x18541daf8 <+20>:  cmp    x2, #0x2
    0x18541dafc <+24>:  mov    x8, #0x404d000000000000   ; =4633359591634108416 
    0x18541db00 <+28>:  fmov   d0, x8
    0x18541db04 <+32>:  mov    x8, #0x404e000000000000   ; =4633641066610819072 
    0x18541db08 <+36>:  fmov   d1, x8
    0x18541db0c <+40>:  fcsel  d3, d1, d0, eq
    0x18541db10 <+44>:  adrp   x8, 389766
    0x18541db14 <+48>:  ldr    x8, [x8, #0x9c0]
    0x18541db18 <+52>:  stp    x0, x8, [sp]
    0x18541db1c <+56>:  adrp   x8, 461219
    0x18541db20 <+60>:  add    x1, x8, #0x108
    0x18541db24 <+64>:  mov    x8, #0x4074000000000000   ; =4644337115725824000 
    0x18541db28 <+68>:  fmov   d2, x8
    0x18541db2c <+72>:  mov    x0, sp
    0x18541db30 <+76>:  movi   d0, #0000000000000000
    0x18541db34 <+80>:  movi   d1, #0000000000000000
    0x18541db38 <+84>:  bl     0x18617d534               ; symbol stub for: objc_msgSendSuper2
    0x18541db3c <+88>:  mov    x20, x0
    0x18541db40 <+92>:  cbz    x0, 0x18541db5c           ; <+120>
    0x18541db44 <+96>:  adrp   x8, 437120
    0x18541db48 <+100>: ldrsw  x8, [x8, #0x800]
    0x18541db4c <+104>: str    x19, [x20, x8]
    0x18541db50 <+108>: mov    x0, x20
    0x18541db54 <+112>: mov    w2, #0x2                  ; =2 
    0x18541db58 <+116>: bl     0x1869a26e0               ; objc_msgSend$setAutoresizingMask:
    0x18541db5c <+120>: mov    x0, x20
    0x18541db60 <+124>: ldp    x29, x30, [sp, #0x20]
    0x18541db64 <+128>: ldp    x20, x19, [sp, #0x10]
    0x18541db68 <+132>: add    sp, sp, #0x30
    0x18541db6c <+136>: ret    
```

### didMoveToSuperview

```
UIKitCore`-[UIRefreshControl didMoveToSuperview]:
    0x18541e00c <+0>:   sub    sp, sp, #0x40
    0x18541e010 <+4>:   stp    x22, x21, [sp, #0x10]
    0x18541e014 <+8>:   stp    x20, x19, [sp, #0x20]
    0x18541e018 <+12>:  stp    x29, x30, [sp, #0x30]
    0x18541e01c <+16>:  add    x29, sp, #0x30
    0x18541e020 <+20>:  mov    x19, x0
    0x18541e024 <+24>:  bl     0x1869eecc0               ; objc_msgSend$superview
    0x18541e028 <+28>:  bl     0x18617d444               ; symbol stub for: objc_claimAutoreleasedReturnValue
    0x18541e02c <+32>:  mov    x20, x0
    0x18541e030 <+36>:  bl     0x18617d5c4               ; symbol stub for: objc_release_x20
    0x18541e034 <+40>:  cbz    x20, 0x18541e120          ; <+276>
    0x18541e038 <+44>:  adrp   x8, 437119
    0x18541e03c <+48>:  ldrsw  x22, [x8, #0x808]
    0x18541e040 <+52>:  ldr    x8, [x19, x22]
    0x18541e044 <+56>:  cbnz   x8, 0x18541e100           ; <+244>
    0x18541e048 <+60>:  mov    x0, x19
    0x18541e04c <+64>:  bl     0x186868ec0               ; objc_msgSend$_containingScrollView
    0x18541e050 <+68>:  bl     0x18617d444               ; symbol stub for: objc_claimAutoreleasedReturnValue
    0x18541e054 <+72>:  mov    x20, x0
    0x18541e058 <+76>:  cbz    x0, 0x18541e0b0           ; <+164>
    0x18541e05c <+80>:  adrp   x8, 437167
    0x18541e060 <+84>:  add    x0, x8, #0xc20            ; (void *)0x00000001effcdc48: _UIScrollViewRefreshControlHost
    0x18541e064 <+88>:  bl     0x18617d3d8               ; symbol stub for: objc_alloc
    0x18541e068 <+92>:  mov    x2, x20
    0x18541e06c <+96>:  bl     0x186951b40               ; objc_msgSend$initWithScrollView:
    0x18541e070 <+100>: ldr    x8, [x19, x22]
    0x18541e074 <+104>: str    x0, [x19, x22]
    0x18541e078 <+108>: bl     0x18617d648               ; symbol stub for: objc_release_x8
    0x18541e07c <+112>: mov    x0, x19
    0x18541e080 <+116>: bl     0x1869e7620               ; objc_msgSend$sizeToFit
    0x18541e084 <+120>: mov    x0, x19
    0x18541e088 <+124>: bl     0x18693b660               ; objc_msgSend$frame
    0x18541e08c <+128>: adrp   x8, 437119
    0x18541e090 <+132>: ldrsw  x8, [x8, #0x814]
    0x18541e094 <+136>: str    d3, [x19, x8]
    0x18541e098 <+140>: mov    x0, x19
    0x18541e09c <+144>: bl     0x186869e40               ; objc_msgSend$_contentView
    0x18541e0a0 <+148>: bl     0x18617d444               ; symbol stub for: objc_claimAutoreleasedReturnValue
    0x18541e0a4 <+152>: mov    x21, x0
    0x18541e0a8 <+156>: bl     0x18698b6c0               ; objc_msgSend$refreshControlInvalidatedSnappingHeight
    0x18541e0ac <+160>: bl     0x18617d5d0               ; symbol stub for: objc_release_x21
    0x18541e0b0 <+164>: bl     0x18617d5c4               ; symbol stub for: objc_release_x20
    0x18541e0b4 <+168>: ldr    x8, [x19, x22]
    0x18541e0b8 <+172>: cbnz   x8, 0x18541e100           ; <+244>
    0x18541e0bc <+176>: adrp   x8, 388724
    0x18541e0c0 <+180>: ldr    x20, [x8, #0x790]
    0x18541e0c4 <+184>: adrp   x8, 388723
    0x18541e0c8 <+188>: ldr    x8, [x8, #0xb68]
    0x18541e0cc <+192>: ldr    x21, [x8]
    0x18541e0d0 <+196>: mov    x0, x19
    0x18541e0d4 <+200>: bl     0x18617d540               ; symbol stub for: objc_opt_class
    0x18541e0d8 <+204>: bl     0x18617bfa4               ; symbol stub for: NSStringFromClass
    0x18541e0dc <+208>: bl     0x18617d444               ; symbol stub for: objc_claimAutoreleasedReturnValue
    0x18541e0e0 <+212>: mov    x22, x0
    0x18541e0e4 <+216>: str    x0, [sp]
    0x18541e0e8 <+220>: adrp   x3, 388887
    0x18541e0ec <+224>: add    x3, x3, #0x578            ; @"%@ was unable to find its associated scroll view"
    0x18541e0f0 <+228>: mov    x0, x20
    0x18541e0f4 <+232>: mov    x2, x21
    0x18541e0f8 <+236>: bl     0x1869891e0               ; objc_msgSend$raise:format:
    0x18541e0fc <+240>: bl     0x18617d5dc               ; symbol stub for: objc_release_x22
    0x18541e100 <+244>: mov    x0, x19
    0x18541e104 <+248>: bl     0x1868e79e0               ; objc_msgSend$_updateSnappingHeight
->  0x18541e108 <+252>: mov    x0, x19
    0x18541e10c <+256>: ldp    x29, x30, [sp, #0x30]
    0x18541e110 <+260>: ldp    x20, x19, [sp, #0x20]
    0x18541e114 <+264>: ldp    x22, x21, [sp, #0x10]
    0x18541e118 <+268>: add    sp, sp, #0x40
    0x18541e11c <+272>: b      0x1868ded60               ; objc_msgSend$_update
    0x18541e120 <+276>: ldp    x29, x30, [sp, #0x30]
    0x18541e124 <+280>: ldp    x20, x19, [sp, #0x20]
    0x18541e128 <+284>: ldp    x22, x21, [sp, #0x10]
    0x18541e12c <+288>: add    sp, sp, #0x40
    0x18541e130 <+292>: ret    
```

### _update

```
UIKitCore`-[UIRefreshControl _update]:
->  0x18541eb44 <+0>:   stp    d13, d12, [sp, #-0x60]!
    0x18541eb48 <+4>:   stp    d11, d10, [sp, #0x10]
    0x18541eb4c <+8>:   stp    d9, d8, [sp, #0x20]
    0x18541eb50 <+12>:  stp    x22, x21, [sp, #0x30]
    0x18541eb54 <+16>:  stp    x20, x19, [sp, #0x40]
    0x18541eb58 <+20>:  stp    x29, x30, [sp, #0x50]
    0x18541eb5c <+24>:  add    x29, sp, #0x50
    0x18541eb60 <+28>:  mov    x19, x0
    0x18541eb64 <+32>:  adrp   x8, 437119
    0x18541eb68 <+36>:  ldrsw  x8, [x8, #0x828]
    0x18541eb6c <+40>:  ldrb   w8, [x0, x8]
    0x18541eb70 <+44>:  cbnz   w8, 0x18541ec3c           ; <+248>
    0x18541eb74 <+48>:  mov    x0, x19
    0x18541eb78 <+52>:  bl     0x18693b660               ; objc_msgSend$frame
    0x18541eb7c <+56>:  fmov   d8, d3
    0x18541eb80 <+60>:  adrp   x8, 437119
    0x18541eb84 <+64>:  ldrsw  x21, [x8, #0x808]
    0x18541eb88 <+68>:  ldr    x0, [x19, x21]
    0x18541eb8c <+72>:  bl     0x186998620               ; objc_msgSend$scrollView
    0x18541eb90 <+76>:  bl     0x18617d444               ; symbol stub for: objc_claimAutoreleasedReturnValue
    0x18541eb94 <+80>:  mov    x20, x0
    0x18541eb98 <+84>:  bl     0x186916f00               ; objc_msgSend$contentOffset
    0x18541eb9c <+88>:  fmov   d9, d0
    0x18541eba0 <+92>:  fmov   d10, d1
    0x18541eba4 <+96>:  bl     0x18617d5c4               ; symbol stub for: objc_release_x20
    0x18541eba8 <+100>: mov    x0, x19
    0x18541ebac <+104>: fmov   d0, d9
    0x18541ebb0 <+108>: fmov   d1, d10
    0x18541ebb4 <+112>: bl     0x1868a04a0               ; objc_msgSend$_originForContentOffset:
    0x18541ebb8 <+116>: fmov   d11, d0
    0x18541ebbc <+120>: fmov   d12, d1
    0x18541ebc0 <+124>: ldr    x0, [x19, x21]
    0x18541ebc4 <+128>: bl     0x186998620               ; objc_msgSend$scrollView
    0x18541ebc8 <+132>: bl     0x18617d444               ; symbol stub for: objc_claimAutoreleasedReturnValue
    0x18541ebcc <+136>: mov    x20, x0
    0x18541ebd0 <+140>: bl     0x186906f00               ; objc_msgSend$bounds
    0x18541ebd4 <+144>: fmov   d13, d2
    0x18541ebd8 <+148>: bl     0x18617d5c4               ; symbol stub for: objc_release_x20
    0x18541ebdc <+152>: ldr    x0, [x19, x21]
    0x18541ebe0 <+156>: bl     0x18698b6a0               ; objc_msgSend$refreshControlInsetsAffectScrollViewRubberBanding
    0x18541ebe4 <+160>: cbz    w0, 0x18541ec00           ; <+188>
    0x18541ebe8 <+164>: mov    x0, x19
    0x18541ebec <+168>: fmov   d0, d11
    0x18541ebf0 <+172>: fmov   d1, d12
    0x18541ebf4 <+176>: fmov   d2, d13
    0x18541ebf8 <+180>: fmov   d3, d8
    0x18541ebfc <+184>: bl     0x1869b3760               ; objc_msgSend$setFrame:
    0x18541ec00 <+188>: mov    x0, x19
    0x18541ec04 <+192>: fmov   d0, d9
    0x18541ec08 <+196>: fmov   d1, d10
    0x18541ec0c <+200>: fmov   d2, d11
    0x18541ec10 <+204>: fmov   d3, d12
    0x18541ec14 <+208>: bl     0x1868ecb20               ; objc_msgSend$_visibleHeightForContentOffset:origin:
    0x18541ec18 <+212>: fmov   d8, d0
    0x18541ec1c <+216>: mov    x0, x19
    0x18541ec20 <+220>: bl     0x1868c95a0               ; objc_msgSend$_setVisibleHeight:
    0x18541ec24 <+224>: fcmp   d8, #0.0
    0x18541ec28 <+228>: b.ne   0x18541ec3c               ; <+248>
    0x18541ec2c <+232>: mov    x0, x19
    0x18541ec30 <+236>: bl     0x1868e0900               ; objc_msgSend$_updateConcealingMask
    0x18541ec34 <+240>: mov    x0, x19
    0x18541ec38 <+244>: bl     0x1868e3700               ; objc_msgSend$_updateHiddenStateIfNeeded
    0x18541ec3c <+248>: adrp   x8, 437119
    0x18541ec40 <+252>: ldrsw  x8, [x8, #0x800]
    0x18541ec44 <+256>: ldr    x8, [x19, x8]
    0x18541ec48 <+260>: cmp    x8, #0x2
    0x18541ec4c <+264>: b.ne   0x18541eccc               ; <+392>
    0x18541ec50 <+268>: adrp   x21, 437119
    0x18541ec54 <+272>: add    x21, x21, #0x804          ; _MergedGlobals + 4
    0x18541ec58 <+276>: ldrsw  x8, [x21, #0x4]
    0x18541ec5c <+280>: ldr    x0, [x19, x8]
    0x18541ec60 <+284>: bl     0x186998620               ; objc_msgSend$scrollView
    0x18541ec64 <+288>: bl     0x18617d444               ; symbol stub for: objc_claimAutoreleasedReturnValue
    0x18541ec68 <+292>: mov    x20, x0
    0x18541ec6c <+296>: bl     0x1868eb5c0               ; objc_msgSend$_verticalVelocity
    0x18541ec70 <+300>: fmov   d8, d0
    0x18541ec74 <+304>: bl     0x18617d5c4               ; symbol stub for: objc_release_x20
    0x18541ec78 <+308>: mov    x0, x19
    0x18541ec7c <+312>: fmov   d0, d8
    0x18541ec80 <+316>: bl     0x1868d37a0               ; objc_msgSend$_stiffnessForVelocity:
    0x18541ec84 <+320>: fmov   d9, d0
    0x18541ec88 <+324>: mov    x0, x19
    0x18541ec8c <+328>: fmov   d0, d8
    0x18541ec90 <+332>: bl     0x186888760               ; objc_msgSend$_impactIntensityForVelocity:
    0x18541ec94 <+336>: fmov   d8, d0
    0x18541ec98 <+340>: ldrsw  x20, [x21]
    0x18541ec9c <+344>: ldr    x0, [x19, x20]
    0x18541eca0 <+348>: fmov   d0, d9
    0x18541eca4 <+352>: bl     0x1869aa1a0               ; objc_msgSend$setCurrentPopStiffness:
    0x18541eca8 <+356>: ldr    x0, [x19, x20]
    0x18541ecac <+360>: fmov   d0, d8
    0x18541ecb0 <+364>: ldp    x29, x30, [sp, #0x50]
    0x18541ecb4 <+368>: ldp    x20, x19, [sp, #0x40]
    0x18541ecb8 <+372>: ldp    x22, x21, [sp, #0x30]
    0x18541ecbc <+376>: ldp    d9, d8, [sp, #0x20]
    0x18541ecc0 <+380>: ldp    d11, d10, [sp, #0x10]
    0x18541ecc4 <+384>: ldp    d13, d12, [sp], #0x60
    0x18541ecc8 <+388>: b      0x1869b7aa0               ; objc_msgSend$setImpactIntensity:
    0x18541eccc <+392>: ldp    x29, x30, [sp, #0x50]
    0x18541ecd0 <+396>: ldp    x20, x19, [sp, #0x40]
    0x18541ecd4 <+400>: ldp    x22, x21, [sp, #0x30]
    0x18541ecd8 <+404>: ldp    d9, d8, [sp, #0x20]
    0x18541ecdc <+408>: ldp    d11, d10, [sp, #0x10]
    0x18541ece0 <+412>: ldp    d13, d12, [sp], #0x60
    0x18541ece4 <+416>: ret    

```

### _setVisibleHeight:

```
UIKitCore`-[UIRefreshControl _setVisibleHeight:]:
    0x18541e76c <+0>:  stp    x20, x19, [sp, #-0x20]!
    0x18541e770 <+4>:  stp    x29, x30, [sp, #0x10]
    0x18541e774 <+8>:  add    x29, sp, #0x10
    0x18541e778 <+12>: adrp   x8, 437119
    0x18541e77c <+16>: ldrsw  x8, [x8, #0x810]
    0x18541e780 <+20>: ldr    d1, [x0, x8]
    0x18541e784 <+24>: fcmp   d1, d0
    0x18541e788 <+28>: b.eq   0x18541e7c4               ; <+88>
    0x18541e78c <+32>: mov    x19, x0
    0x18541e790 <+36>: str    d0, [x0, x8]
    0x18541e794 <+40>: bl     0x1868ac660               ; objc_msgSend$_recomputeNewState
    0x18541e798 <+44>: mov    x2, x0
    0x18541e79c <+48>: mov    x0, x19
    0x18541e7a0 <+52>: bl     0x1869ca640               ; objc_msgSend$setRefreshControlState:
->  0x18541e7a4 <+56>: mov    x0, x19
    0x18541e7a8 <+60>: bl     0x1869c2860               ; objc_msgSend$setNeedsLayout
    0x18541e7ac <+64>: mov    x0, x19
    0x18541e7b0 <+68>: bl     0x1868e3700               ; objc_msgSend$_updateHiddenStateIfNeeded
    0x18541e7b4 <+72>: mov    x0, x19
    0x18541e7b8 <+76>: ldp    x29, x30, [sp, #0x10]
    0x18541e7bc <+80>: ldp    x20, x19, [sp], #0x20
    0x18541e7c0 <+84>: b      0x1868e0900               ; objc_msgSend$_updateConcealingMask
    0x18541e7c4 <+88>: ldp    x29, x30, [sp, #0x10]
    0x18541e7c8 <+92>: ldp    x20, x19, [sp], #0x20
    0x18541e7cc <+96>: ret    
```

### _setRefreshControlState:notify:

```
UIKitCore`-[UIRefreshControl _setRefreshControlState:notify:]:
    0x18541f3d0 <+0>:   sub    sp, sp, #0x50
    0x18541f3d4 <+4>:   stp    x24, x23, [sp, #0x10]
    0x18541f3d8 <+8>:   stp    x22, x21, [sp, #0x20]
    0x18541f3dc <+12>:  stp    x20, x19, [sp, #0x30]
    0x18541f3e0 <+16>:  stp    x29, x30, [sp, #0x40]
    0x18541f3e4 <+20>:  add    x29, sp, #0x40
    0x18541f3e8 <+24>:  mov    x21, x3
    0x18541f3ec <+28>:  mov    x20, x2
    0x18541f3f0 <+32>:  mov    x19, x0
    0x18541f3f4 <+36>:  cmp    x2, #0x7
    0x18541f3f8 <+40>:  b.hs   0x18541f504               ; <+308>
    0x18541f3fc <+44>:  adrp   x8, 437118
    0x18541f400 <+48>:  ldrsw  x24, [x8, #0x80c]
    0x18541f404 <+52>:  ldr    x2, [x19, x24]
    0x18541f408 <+56>:  mov    x0, x19
    0x18541f40c <+60>:  mov    x3, x20
    0x18541f410 <+64>:  bl     0x186860380               ; objc_msgSend$_canTransitionFromState:toState:
    0x18541f414 <+68>:  cbz    w0, 0x18541f49c           ; <+204>
    0x18541f418 <+72>:  ldr    x22, [x19, x24]
    0x18541f41c <+76>:  sub    x8, x20, #0x4
    0x18541f420 <+80>:  cmn    x8, #0x3
    0x18541f424 <+84>:  b.hi   0x18541f430               ; <+96>
    0x18541f428 <+88>:  mov    x0, x19
    0x18541f42c <+92>:  bl     0x1868af9a0               ; objc_msgSend$_removeInsets
    0x18541f430 <+96>:  mov    x0, x19
    0x18541f434 <+100>: bl     0x186869e40               ; objc_msgSend$_contentView
    0x18541f438 <+104>: bl     0x18617d444               ; symbol stub for: objc_claimAutoreleasedReturnValue
    0x18541f43c <+108>: mov    x23, x0
    0x18541f440 <+112>: mov    x2, x22
    0x18541f444 <+116>: mov    x3, x20
    0x18541f448 <+120>: bl     0x186a0fae0               ; objc_msgSend$willTransitionFromState:toState:
    0x18541f44c <+124>: bl     0x18617d5e8               ; symbol stub for: objc_release_x23
    0x18541f450 <+128>: str    x20, [x19, x24]
    0x18541f454 <+132>: mov    x0, x19
    0x18541f458 <+136>: bl     0x186869e40               ; objc_msgSend$_contentView
    0x18541f45c <+140>: bl     0x18617d444               ; symbol stub for: objc_claimAutoreleasedReturnValue
    0x18541f460 <+144>: mov    x23, x0
    0x18541f464 <+148>: mov    x2, x22
    0x18541f468 <+152>: mov    x3, x20
    0x18541f46c <+156>: bl     0x186927720               ; objc_msgSend$didTransitionFromState:toState:
->  0x18541f470 <+160>: bl     0x18617d5e8               ; symbol stub for: objc_release_x23
    0x18541f474 <+164>: ldr    x8, [x19, x24]
    0x18541f478 <+168>: cmp    x8, x20
    0x18541f47c <+172>: b.ne   0x18541f49c               ; <+204>
    0x18541f480 <+176>: cmp    x20, #0x3
    0x18541f484 <+180>: b.eq   0x18541f4b4               ; <+228>
    0x18541f488 <+184>: cmp    x20, #0x2
    0x18541f48c <+188>: b.ne   0x18541f4cc               ; <+252>
    0x18541f490 <+192>: mov    x0, x19
    0x18541f494 <+196>: bl     0x186853480               ; objc_msgSend$_addInsets
    0x18541f498 <+200>: b      0x18541f4cc               ; <+252>
    0x18541f49c <+204>: ldp    x29, x30, [sp, #0x40]
    0x18541f4a0 <+208>: ldp    x20, x19, [sp, #0x30]
    0x18541f4a4 <+212>: ldp    x22, x21, [sp, #0x20]
    0x18541f4a8 <+216>: ldp    x24, x23, [sp, #0x10]
    0x18541f4ac <+220>: add    sp, sp, #0x50
    0x18541f4b0 <+224>: ret    
    0x18541f4b4 <+228>: mov    x0, x19
    0x18541f4b8 <+232>: bl     0x186853480               ; objc_msgSend$_addInsets
    0x18541f4bc <+236>: cbz    w21, 0x18541f4cc          ; <+252>
    0x18541f4c0 <+240>: mov    x0, x19
    0x18541f4c4 <+244>: mov    w2, #0x1000               ; =4096 
    0x18541f4c8 <+248>: bl     0x18699c6c0               ; objc_msgSend$sendActionsForControlEvents:
    0x18541f4cc <+252>: adrp   x8, 437118
    0x18541f4d0 <+256>: ldrsw  x8, [x8, #0x808]
    0x18541f4d4 <+260>: ldr    x0, [x19, x8]
    0x18541f4d8 <+264>: mov    x2, x19
    0x18541f4dc <+268>: mov    x3, x20
    0x18541f4e0 <+272>: mov    x4, x22
    0x18541f4e4 <+276>: bl     0x18698b660               ; objc_msgSend$refreshControl:didChangeToState:fromState:
    0x18541f4e8 <+280>: mov    x0, x19
    0x18541f4ec <+284>: ldp    x29, x30, [sp, #0x40]
    0x18541f4f0 <+288>: ldp    x20, x19, [sp, #0x30]
    0x18541f4f4 <+292>: ldp    x22, x21, [sp, #0x20]
    0x18541f4f8 <+296>: ldp    x24, x23, [sp, #0x10]
    0x18541f4fc <+300>: add    sp, sp, #0x50
    0x18541f500 <+304>: b      0x1869c2860               ; objc_msgSend$setNeedsLayout
    0x18541f504 <+308>: mov    x22, x1
    0x18541f508 <+312>: adrp   x8, 388723
    0x18541f50c <+316>: ldr    x0, [x8, #0x650]
    0x18541f510 <+320>: bl     0x18691b8a0               ; objc_msgSend$currentHandler
    0x18541f514 <+324>: bl     0x18617d444               ; symbol stub for: objc_claimAutoreleasedReturnValue
    0x18541f518 <+328>: mov    x23, x0
    0x18541f51c <+332>: str    x20, [sp]
    0x18541f520 <+336>: adrp   x4, 388886
    0x18541f524 <+340>: add    x4, x4, #0x598            ; @"UIRefreshControl.m"
    0x18541f528 <+344>: adrp   x6, 388886
    0x18541f52c <+348>: add    x6, x6, #0x5d8            ; @"Illegal state: %ld"
    0x18541f530 <+352>: mov    x2, x22
    0x18541f534 <+356>: mov    x3, x19
    0x18541f538 <+360>: mov    w5, #0x316                ; =790 
    0x18541f53c <+364>: bl     0x18693f7e0               ; objc_msgSend$handleFailureInMethod:object:file:lineNumber:description:
    0x18541f540 <+368>: bl     0x18617d5e8               ; symbol stub for: objc_release_x23
    0x18541f544 <+372>: b      0x18541f3fc               ; <+44>
```

### _addInsets

```
UIKitCore`-[UIRefreshControl _addInsets]:
->  0x18541ece8 <+0>:  stp    x20, x19, [sp, #-0x20]!
    0x18541ecec <+4>:  stp    x29, x30, [sp, #0x10]
    0x18541ecf0 <+8>:  add    x29, sp, #0x10
    0x18541ecf4 <+12>: mov    x19, x0
    0x18541ecf8 <+16>: bl     0x1868ad380               ; objc_msgSend$_refreshControlHeight
    0x18541ecfc <+20>: mov    x0, x19
    0x18541ed00 <+24>: ldp    x29, x30, [sp, #0x10]
    0x18541ed04 <+28>: ldp    x20, x19, [sp], #0x20
    0x18541ed08 <+32>: b      0x186853460               ; objc_msgSend$_addInsetHeight:
```

### _addInsetHeight

```
(lldb) po $d0
60
```

```
UIKitCore`-[UIRefreshControl _addInsetHeight:]:
->  0x18541ed30 <+0>:   fcmp   d0, #0.0
    0x18541ed34 <+4>:   b.le   0x18541edac               ; <+124>
    0x18541ed38 <+8>:   stp    x20, x19, [sp, #-0x20]!
    0x18541ed3c <+12>:  stp    x29, x30, [sp, #0x10]
    0x18541ed40 <+16>:  add    x29, sp, #0x10
    0x18541ed44 <+20>:  mov    x19, x0
    0x18541ed48 <+24>:  adrp   x8, 437119
    0x18541ed4c <+28>:  ldrsw  x8, [x8, #0x81c]
    0x18541ed50 <+32>:  ldrb   w9, [x0, x8]
    0x18541ed54 <+36>:  cbnz   w9, 0x18541eda4           ; <+116>
    0x18541ed58 <+40>:  adrp   x9, 437119
    0x18541ed5c <+44>:  ldrsw  x9, [x9, #0x808]
    0x18541ed60 <+48>:  ldr    x10, [x19, x9]
    0x18541ed64 <+52>:  cbz    x10, 0x18541eda4          ; <+116>
    0x18541ed68 <+56>:  adrp   x10, 437119
    0x18541ed6c <+60>:  add    x10, x10, #0x820          ; _MergedGlobals + 32
    0x18541ed70 <+64>:  ldrsw  x11, [x10]
    0x18541ed74 <+68>:  ldr    d1, [x19, x11]
    0x18541ed78 <+72>:  fadd   d1, d1, d0
    0x18541ed7c <+76>:  str    d1, [x19, x11]
    0x18541ed80 <+80>:  mov    w11, #0x1                 ; =1 
    0x18541ed84 <+84>:  strb   w11, [x19, x8]
    0x18541ed88 <+88>:  ldrsw  x20, [x10, #0x8]
    0x18541ed8c <+92>:  strb   w11, [x19, x20]
    0x18541ed90 <+96>:  ldrsw  x8, [x10, #0x4]
    0x18541ed94 <+100>: str    d0, [x19, x8]
    0x18541ed98 <+104>: ldr    x0, [x19, x9]
    0x18541ed9c <+108>: bl     0x186947f00               ; objc_msgSend$incrementInsetHeight:
    0x18541eda0 <+112>: strb   wzr, [x19, x20]
    0x18541eda4 <+116>: ldp    x29, x30, [sp, #0x10]
    0x18541eda8 <+120>: ldp    x20, x19, [sp], #0x20
    0x18541edac <+124>: ret    

```

# _UIScrollViewRefreshControlHost

## Runtime headers

https://github.com/nst/iOS-Runtime-Headers/blob/master/PrivateFrameworks/UIKitCore.framework/_UIScrollViewRefreshControlHost.h

## Stack traces

### incrementInsetHeight:

```
UIKitCore`-[_UIScrollViewRefreshControlHost incrementInsetHeight:]:
->  0x185451964 <+0>:  sub    sp, sp, #0x30
    0x185451968 <+4>:  stp    d9, d8, [sp, #0x10]
    0x18545196c <+8>:  stp    x29, x30, [sp, #0x20]
    0x185451970 <+12>: add    x29, sp, #0x20
    0x185451974 <+16>: fmov   d8, d0
    0x185451978 <+20>: add    x0, x0, #0x8
    0x18545197c <+24>: bl     0x18617d504               ; symbol stub for: objc_loadWeakRetained
    0x185451980 <+28>: str    x0, [sp, #0x8]
    0x185451984 <+32>: fmov   d0, d8
    0x185451988 <+36>: bl     0x186853920               ; objc_msgSend$_addRefreshInset:
    0x18545198c <+40>: ldr    x0, [sp, #0x8]
    0x185451990 <+44>: ldp    x29, x30, [sp, #0x20]
    0x185451994 <+48>: ldp    d9, d8, [sp, #0x10]
    0x185451998 <+52>: add    sp, sp, #0x30
    0x18545199c <+56>: b      0x18617d588               ; symbol stub for: objc_release
```

# _UIRefreshControlContentView

Legacy Content View

# _UIRefreshControlModernContentView

## Runtime headers

https://github.com/nst/iOS-Runtime-Headers/blob/master/PrivateFrameworks/UIKitCore.framework/_UIRefreshControlModernContentView.h

## Values

|property|value|
|---|---|
|maximumSnappingHeight|150.3301056338028|
|_maximumSnappingHeightScalingForScrollViewHeight|1.336267605633803|
|_heightAtWhichNoneOfTheInterfaceElementsAreVisibleEvenIfTheControlIsStillPartiallyOnScreen|5|

## Stack traces

### didTransitionFromState:toState:

```
UIKitCore`-[_UIRefreshControlModernContentView didTransitionFromState:toState:]:
    0x18544ffa8 <+0>:   sub    sp, sp, #0x50
    0x18544ffac <+4>:   stp    x24, x23, [sp, #0x10]
    0x18544ffb0 <+8>:   stp    x22, x21, [sp, #0x20]
    0x18544ffb4 <+12>:  stp    x20, x19, [sp, #0x30]
    0x18544ffb8 <+16>:  stp    x29, x30, [sp, #0x40]
    0x18544ffbc <+20>:  add    x29, sp, #0x40
    0x18544ffc0 <+24>:  mov    x19, x3
    0x18544ffc4 <+28>:  mov    x20, x2
    0x18544ffc8 <+32>:  mov    x21, x0
    0x18544ffcc <+36>:  cmp    x3, #0x6
    0x18544ffd0 <+40>:  b.hi   0x1854500c0               ; <+280>
    0x18544ffd4 <+44>:  adrp   x8, 3741
    0x18544ffd8 <+48>:  add    x8, x8, #0x358            ; fittingSizeWithChicletSize:._sizeBuckets + 376
    0x18544ffdc <+52>:  adr    x9, 0x18544ffec           ; <+68>
    0x18544ffe0 <+56>:  ldrb   w10, [x8, x19]
    0x18544ffe4 <+60>:  add    x9, x9, x10, lsl #2
    0x18544ffe8 <+64>:  br     x9
    0x18544ffec <+68>:  cmp    x20, #0x4
    0x18544fff0 <+72>:  b.eq   0x185450054               ; <+172>
    0x18544fff4 <+76>:  mov    x0, x21
    0x18544fff8 <+80>:  bl     0x1868e88c0               ; objc_msgSend$_updateTimeOffsetOfRelevantLayers
    0x18544fffc <+84>:  b      0x1854500c0               ; <+280>
    0x185450000 <+88>:  mov    x0, x21
    0x185450004 <+92>:  bl     0x1869476c0               ; objc_msgSend$impactFeedbackGenerator
    0x185450008 <+96>:  bl     0x18617d444               ; symbol stub for: objc_claimAutoreleasedReturnValue
    0x18545000c <+100>: mov    x22, x0
    0x185450010 <+104>: bl     0x18695a9e0               ; objc_msgSend$isActive
    0x185450014 <+108>: mov    x23, x0
    0x185450018 <+112>: bl     0x18617d5dc               ; symbol stub for: objc_release_x22
    0x18545001c <+116>: tbnz   w23, #0x0, 0x18545003c    ; <+148>
    0x185450020 <+120>: mov    x0, x21
    0x185450024 <+124>: bl     0x1869476c0               ; objc_msgSend$impactFeedbackGenerator
    0x185450028 <+128>: bl     0x18617d444               ; symbol stub for: objc_claimAutoreleasedReturnValue
    0x18545002c <+132>: mov    x22, x0
    0x185450030 <+136>: mov    x2, #0x0                  ; =0 
    0x185450034 <+140>: bl     0x1868f2400               ; objc_msgSend$activateWithCompletionBlock:
    0x185450038 <+144>: bl     0x18617d5dc               ; symbol stub for: objc_release_x22
    0x18545003c <+148>: mov    x0, x21
    0x185450040 <+152>: bl     0x1868d1320               ; objc_msgSend$_snappingMagic
->  0x185450044 <+156>: b      0x18545004c               ; <+164>
    0x185450048 <+160>: cbz    x20, 0x1854500b8          ; <+272>
    0x18545004c <+164>: cmp    x20, #0x4
    0x185450050 <+168>: b.ne   0x1854500c0               ; <+280>
    0x185450054 <+172>: mov    x0, x21
    0x185450058 <+176>: bl     0x1868b2740               ; objc_msgSend$_resetToRevealingState
    0x18545005c <+180>: b      0x1854500c0               ; <+280>
    0x185450060 <+184>: mov    x0, x21
    0x185450064 <+188>: bl     0x1868828a0               ; objc_msgSend$_goAway
    0x185450068 <+192>: b      0x18545007c               ; <+212>
    0x18545006c <+196>: cmp    x20, #0x4
    0x185450070 <+200>: b.ne   0x18545007c               ; <+212>
    0x185450074 <+204>: mov    x0, x21
    0x185450078 <+208>: bl     0x1868b2740               ; objc_msgSend$_resetToRevealingState
    0x18545007c <+212>: mov    x0, x21
    0x185450080 <+216>: bl     0x1869476c0               ; objc_msgSend$impactFeedbackGenerator
    0x185450084 <+220>: bl     0x18617d444               ; symbol stub for: objc_claimAutoreleasedReturnValue
    0x185450088 <+224>: mov    x22, x0
    0x18545008c <+228>: bl     0x18695a9e0               ; objc_msgSend$isActive
    0x185450090 <+232>: mov    x23, x0
    0x185450094 <+236>: bl     0x18617d5dc               ; symbol stub for: objc_release_x22
    0x185450098 <+240>: cbz    w23, 0x1854500c0          ; <+280>
    0x18545009c <+244>: mov    x0, x21
    0x1854500a0 <+248>: bl     0x1869476c0               ; objc_msgSend$impactFeedbackGenerator
    0x1854500a4 <+252>: bl     0x18617d444               ; symbol stub for: objc_claimAutoreleasedReturnValue
    0x1854500a8 <+256>: mov    x22, x0
    0x1854500ac <+260>: bl     0x18691e7a0               ; objc_msgSend$deactivate
    0x1854500b0 <+264>: bl     0x18617d5dc               ; symbol stub for: objc_release_x22
    0x1854500b4 <+268>: b      0x1854500c0               ; <+280>
    0x1854500b8 <+272>: mov    x0, x21
    0x1854500bc <+276>: bl     0x1868d9780               ; objc_msgSend$_tickDueToProgrammaticRefresh
    0x1854500c0 <+280>: adrp   x8, 389715
    0x1854500c4 <+284>: ldr    x8, [x8, #0xaf0]
    0x1854500c8 <+288>: stp    x21, x8, [sp]
    0x1854500cc <+292>: adrp   x8, 461207
    0x1854500d0 <+296>: add    x1, x8, #0x3eb
    0x1854500d4 <+300>: mov    x0, sp
    0x1854500d8 <+304>: mov    x2, x20
    0x1854500dc <+308>: mov    x3, x19
    0x1854500e0 <+312>: bl     0x18617d534               ; symbol stub for: objc_msgSendSuper2
    0x1854500e4 <+316>: ldp    x29, x30, [sp, #0x40]
    0x1854500e8 <+320>: ldp    x20, x19, [sp, #0x30]
    0x1854500ec <+324>: ldp    x22, x21, [sp, #0x20]
    0x1854500f0 <+328>: ldp    x24, x23, [sp, #0x10]
    0x1854500f4 <+332>: add    sp, sp, #0x50
    0x1854500f8 <+336>: ret    
```

### _snappingMagic

```
UIKitCore`-[_UIRefreshControlModernContentView _snappingMagic]:
    0x185450e48 <+0>:  sub    sp, sp, #0x20
    0x185450e4c <+4>:  stp    x29, x30, [sp, #0x10]
    0x185450e50 <+8>:  add    x29, sp, #0x10
    0x185450e54 <+12>: bl     0x18698b640               ; objc_msgSend$refreshControl
    0x185450e58 <+16>: bl     0x18617d444               ; symbol stub for: objc_claimAutoreleasedReturnValue
    0x185450e5c <+20>: str    x0, [sp, #0x8]
    0x185450e60 <+24>: mov    w2, #0x3                  ; =3 
    0x185450e64 <+28>: bl     0x1869ca640               ; objc_msgSend$setRefreshControlState:
->  0x185450e68 <+32>: ldr    x0, [sp, #0x8]
    0x185450e6c <+36>: ldp    x29, x30, [sp, #0x10]
    0x185450e70 <+40>: add    sp, sp, #0x20
    0x185450e74 <+44>: b      0x18617d588               ; symbol stub for: objc_release
```

### maximumSnappingHeight

```
UIKitCore`-[_UIRefreshControlModernContentView maximumSnappingHeight]:
->  0x185451028 <+0>:  stp    d9, d8, [sp, #-0x30]!
    0x18545102c <+4>:  stp    x20, x19, [sp, #0x10]
    0x185451030 <+8>:  stp    x29, x30, [sp, #0x20]
    0x185451034 <+12>: add    x29, sp, #0x20
    0x185451038 <+16>: mov    x19, x0
    0x18545103c <+20>: adrp   x8, 437068
    0x185451040 <+24>: ldrsw  x8, [x8, #0xbe4]
    0x185451044 <+28>: ldr    x0, [x0, x8]
    0x185451048 <+32>: bl     0x18693b660               ; objc_msgSend$frame
    0x18545104c <+36>: mov    x8, #0x4059000000000000   ; =4636737291354636288 
    0x185451050 <+40>: fmov   d0, x8
    0x185451054 <+44>: fadd   d0, d3, d0
    0x185451058 <+48>: fmov   d1, #1.12500000
    0x18545105c <+52>: fmul   d8, d0, d1
    0x185451060 <+56>: mov    x0, x19
    0x185451064 <+60>: bl     0x18689a6c0               ; objc_msgSend$_maximumSnappingHeightScalingForScrollViewHeight
    0x185451068 <+64>: fmul   d0, d0, d8
    0x18545106c <+68>: ldp    x29, x30, [sp, #0x20]
    0x185451070 <+72>: ldp    x20, x19, [sp, #0x10]
    0x185451074 <+76>: ldp    d9, d8, [sp], #0x30
    0x185451078 <+80>: ret    
```

# UIScrollView

## Stack traces

### adjustedContentInset

```
UIKitCore`-[UIScrollView adjustedContentInset]:
->  0x186036d28 <+0>:  stp    x20, x19, [sp, #-0x20]!
    0x186036d2c <+4>:  stp    x29, x30, [sp, #0x10]
    0x186036d30 <+8>:  add    x29, sp, #0x10
    0x186036d34 <+12>: adrp   x8, 434039
    0x186036d38 <+16>: ldrsw  x8, [x8, #0xb5c]
    0x186036d3c <+20>: add    x19, x0, x8
    0x186036d40 <+24>: bl     0x1868d6660               ; objc_msgSend$_systemContentInset
    0x186036d44 <+28>: ldp    d4, d5, [x19]
    0x186036d48 <+32>: ldp    d6, d7, [x19, #0x10]
    0x186036d4c <+36>: fadd   d0, d4, d0
    0x186036d50 <+40>: fadd   d1, d1, d5
    0x186036d54 <+44>: fadd   d2, d2, d6
    0x186036d58 <+48>: fadd   d3, d3, d7
    0x186036d5c <+52>: ldp    x29, x30, [sp, #0x10]
    0x186036d60 <+56>: ldp    x20, x19, [sp], #0x20
    0x186036d64 <+60>: ret    
```

### _systemContentInset

```
UIKitCore`-[UIScrollView _systemContentInset]:
->  0x18603b350 <+0>: mov    w2, #0x1                  ; =1 
    0x18603b354 <+4>: b      0x1868d6680               ; objc_msgSend$_systemContentInsetIncludingAccessories:
```

### _systemContentInsetIncludingAccessories

### _addRefreshInset:

```
UIKitCore`-[UIScrollView _addRefreshInset:]:
->  0x186037e7c <+0>:   stp    d11, d10, [sp, #-0x40]!
    0x186037e80 <+4>:   stp    d9, d8, [sp, #0x10]
    0x186037e84 <+8>:   stp    x20, x19, [sp, #0x20]
    0x186037e88 <+12>:  stp    x29, x30, [sp, #0x30]
    0x186037e8c <+16>:  add    x29, sp, #0x30
    0x186037e90 <+20>:  fmov   d10, d0
    0x186037e94 <+24>:  mov    x19, x0
    0x186037e98 <+28>:  bl     0x186916f00               ; objc_msgSend$contentOffset
    0x186037e9c <+32>:  fmov   d8, d0
    0x186037ea0 <+36>:  fmov   d9, d1
    0x186037ea4 <+40>:  mov    x0, #0x2                  ; =2 
    0x186037ea8 <+44>:  movk   x0, #0xd, lsl #48
    0x186037eac <+48>:  bl     0x18617cf7c               ; symbol stub for: dyld_program_sdk_at_least
    0x186037eb0 <+52>:  cbz    w0, 0x186037ec8           ; <+76>
    0x186037eb4 <+56>:  adrp   x8, 434038
    0x186037eb8 <+60>:  ldrsw  x8, [x8, #0xb34]
    0x186037ebc <+64>:  ldr    x8, [x19, x8]
    0x186037ec0 <+68>:  cmp    x8, #0x2
    0x186037ec4 <+72>:  b.ne   0x186037ee0               ; <+100>
    0x186037ec8 <+76>:  mov    x0, x19
    0x186037ecc <+80>:  bl     0x186916d20               ; objc_msgSend$contentInset
    0x186037ed0 <+84>:  fadd   d0, d0, d10
    0x186037ed4 <+88>:  mov    x0, x19
    0x186037ed8 <+92>:  bl     0x1869a8400               ; objc_msgSend$setContentInset:
    0x186037edc <+96>:  b      0x186037f04               ; <+136>
    0x186037ee0 <+100>: adrp   x8, 434038
    0x186037ee4 <+104>: ldrsw  x8, [x8, #0xcf8]
    0x186037ee8 <+108>: ldr    d0, [x19, x8]
    0x186037eec <+112>: fadd   d0, d0, d10
    0x186037ef0 <+116>: str    d0, [x19, x8]
    0x186037ef4 <+120>: mov    x0, x19
    0x186037ef8 <+124>: bl     0x1868e2e40               ; objc_msgSend$_updateForChangedScrollRelatedInsets
    0x186037efc <+128>: mov    x0, x19
    0x186037f00 <+132>: bl     0x1868e2e20               ; objc_msgSend$_updateForChangedScrollIndicatorRelatedInsets
    0x186037f04 <+136>: mov    x0, x19
    0x186037f08 <+140>: fmov   d0, d8
    0x186037f0c <+144>: fmov   d1, d9
    0x186037f10 <+148>: ldp    x29, x30, [sp, #0x30]
    0x186037f14 <+152>: ldp    x20, x19, [sp, #0x20]
    0x186037f18 <+156>: ldp    d9, d8, [sp, #0x10]
    0x186037f1c <+160>: ldp    d11, d10, [sp], #0x40
    0x186037f20 <+164>: b      0x1869a85a0               ; objc_msgSend$setContentOffset:
```