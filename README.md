#### Author : [Banyer Han](https://nightfury.info) 

### NRCPrefix
=========
Prefixer for Myanmar National Registration Card's Format

### Match Formats

`[State Number]\[District]([NAING/N])[Register No]`

- `10/lMA(N)123456`
- `10/LAMANA(N)123456`
- `10/lMA(NAING)123456`

Prefer formats
- `10/OUKAMA(N)123456`
- `10/OUKAMA(NAING)123456`
- `၁၀/လမန(နိုင်)၁၂၃၄၅၆`

*NOTE*

Three english characters in district are not complete format and will not support some function.
So you should be use six english characters for district.

## Usage
### Get format

```js
var nrc = MMNRC("10/LaMaNa (NAING) 123456");

nrc.getFormat() // 10/LAMANA(N)123456
nrc.getFormat("mm") // ၁၀/လမန(ႏိုင္)၁၂၃၄၅၆
```

### Test Equal

```js
var nrc = MMNRC("10/LAMANA (N) 123456");

nrc.isEqual('၁၀/လမန((ႏိုင္)၁၂၃၄၅၆') // return true;
```

### Get State name from nrc card

```js
var nrc = MMNRC("10/Lanama(N)123456");

nrc.getState("mm") //မြန္ျပည္နယ္
nrc.getState() // Mon
```
