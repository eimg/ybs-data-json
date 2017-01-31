# YBS Data - Simplify JSON
<div style="font-family: line-height: 1.5em; myanmar3, padauk, 'noto sans myanmar', pyidaungsu, 'myanmar text'">
ရန်ကုန်တိုင်းဒေသကြီး အများပြည်သူ သယ်ယူပို့ဆောင်ရေးကြီးကြပ်မှု အာဏာပိုင်အဖွဲ့ (YRTA) မှ တရားဝင် ထုတ်ပြန်ထားသည့် YBS Open Data (ybs_000115) အား App များ Website များတွင် အသင့် အသုံးပြုနိုင်သော JSON Data အဖြစ် ပြောင်းလဲ ထားခြင်းဖြစ်သည်။
<br><br>
<ul>
	<li>အဓိကအချက်အလက်များနှင့် အသေးစိတ်အချက်အလက်များကို ခွဲထုတ်ထားသည်
	<li>String များအား JSON ဖြစ်အောင် Parse လုပ်ထားသည်
	<li>Whitespace အပိုများ ဖယ်ထုတ်သန့်စင်ထားသည်
	<li>စာလုံးပေါင်းများအချို့ပြင်ဆင်ထားပြီး ဆက်လက်ပြင်ဆင်ရန် ရည်ရွယ်သည်
	<li>မှတ်တိုင်အမည်ကွဲများ တွဲဖက်ထည့်သွင်းထားသည်၊ ဆက်လက်ဖြည့်စွက် သွားရန် ရည်ရွယ်သည်
	<li>တည်နေရာတူ မှတ်တိုင်ကွဲများအား ချိတ်ဆက်ထားသည်
</ul>
</div>
<br>
<img src="http://i.imgur.com/Wmg1pf8.png">
<br>
## List of files
<div style="font-family: line-height: 1.5em;  myanmar3, padauk, 'noto sans myanmar', pyidaungsu, 'myanmar text'">
<ul style="line-height: 1.5em;">
	<li><code>bus-line-data-by-id.js</code>
	<span style="font-family: myanmar3, padauk, 'noto sans myanmar', pyidaungsu, 'myanmar text'">ယာဉ်လိုင်းအလိုက် အခြေပြုမြို့နယ်၊ ဒေသနှင့် အမျိုးအစားများ ပါဝင်သည်</span>
	<li><code>bus-stop-data-by-id.js</code>
	<span style="font-family: myanmar3, padauk, 'noto sans myanmar', pyidaungsu, 'myanmar text'">မှတ်တိုင်အမှတ်အလိုက် အမည်၊ အမည်ကွဲ၊ လမ်းနှင့် တည်နေရာများ ပါဝင်သည်</span>
	<li><code>bus-stop-ids-of-lines.js</code>
	<span style="font-family: myanmar3, padauk, 'noto sans myanmar', pyidaungsu, 'myanmar text'">ယာဉ်လိုင်းအမှတ်အလိုက် ဖြတ်သန်းသွားရောက်သည့် မှတ်တိုင်အမှတ်များ ပါဝင်သည်</span>
	<li><code>bus-stop-names-of-lines.js </code>
	<span style="font-family: myanmar3, padauk, 'noto sans myanmar', pyidaungsu, 'myanmar text'">ယာဉ်လိုင်းအမှတ်အလိုက် ဖြတ်သန်းသွားရောက်သည့် မှတ်တိုင်အမည်များ ပါဝင်သည်</span>
	<li><code>lines-of-bus-stops.js</code>
	<span style="font-family: myanmar3, padauk, 'noto sans myanmar', pyidaungsu, 'myanmar text'">မှတ်တိုင်အလိုက် ဖြတ်သန်းသွားသည့် ယာဉ်လိုင်းများ ပါဝင်သည်</span>
</ul>
</div>

## Route API
<div style="font-family: line-height: 1.5em;  myanmar3, padauk, 'noto sans myanmar', pyidaungsu, 'myanmar text'">
သွားရောက်လိုသည့် ခရီးစဉ် အစမှတ်တိုင် <code>id</code> နှင့် အဆုံးမှတ်တိုင် <code>id</code> ပေးလျှင် စီးရမည့် ယာဉ်လိုင်းများအား ပြန်ပေးနိုင်သည့် လုပ်ဆောင်ချက်ဖြစ်သည်။ အသုံးပြုရန် API URL မှာ အောက်ပါအတိုင်ဖြစ်သည်။
<br><br>
<code><a href="http://barseeyale.com/api/route/best/141/287">http://barseeyale.com/api/route/best/141/287</a></code>
<br><br>
<code>138</code> သည် အစမှတ်တိုင် (လမ်း ၃၀) ဖြစ်သည်။ <code>287</code> သည် အဆုံးမှတ်တိုင် (လှည်းတန်း) ဖြစ်သည်။ မိမိလိုအပ်သည့် ခရီးစဉ်၏ အစမှတ်တိုင်၊ အဆုံးမှတ်တိုင်တို့နှင့် အစားထိုးအသုံးပြုနိုင်သည်။

ရရှိမည့်ရလဒ်နမူနာမှာ အောက်ပါအတိုင်းဖြစ်သည်။<br><br>
<pre style="background: black; color: white">

	{
		"type": 2,
		"line": ["58", "21"],
		"nos": [7, 13],
		"list": [
			["138", "137", "...", "122"],
			["122", "125", "...", "287"]
		],
		"names": ["မော်တင်", "လှည်းတန်း"]
	}
</pre>

<ul>
	<li>
		<code>"type": 2</code> ဆိုသည်မှာ နှစ်ဆင့်စီးရမည်ဟု အဓိပ္ပါယ်ရသည်
	</li>
	<li>
		<code>"line": ["58", "21"]</code> ဆိုသည်မှာ ပထမအဆင့် (၅၈) ကိုစီး၍၊ ဒုတိယအဆင့် (၂၁) ကို ပြောင်းစီးရမည်ဟု အဓိပ္ပါယ်ရသည်
	</li>
	<li>
		<code>"nos": [7, 13]</code> ဆိုသည်မှာ ပထမယာဉ်လိုင်း (၅၈) ကို (၇) မှတ်တိုင်စီး၍၊ ဒုတိယယာဉ်လိုင်း (၂၁) ကို (၁၃) မှတ်တိုင် စီးရမည်ဟု အဓိပ္ပါယ်ရသည်
	</li>
	<li><code>"list"</code> ဖြင့် ဖော်ပြထားသည်များမှာ မှတ်တိုင်စဉ် အဆင့်ဆင့်ဖြစ်သည်</li>
	<li><code>"names": ["မော်တင်", "လှည်းတန်း"]</code> ဆိုသည်မှာ ပထမယာဉ်လိုင်း (၅၈) ကို "မော်တင်" ထိ စီးရမည်ဖြစ်ပြီး၊ ဒုတိယယာဉ်လိုင်း (၂၁) ကို "လှည်းတန်း" ထိ စီးရမည်ဟု အဓိပ္ပါယ်ရသည်
</ul>

API ဆိုင်ရာ ကျန်အချက်အလက်များကို <a href="http://barseeyale.com">barseeyale.com</a> တွင် ဆက်လက်လေ့လာနိုင်သည်။
</div>

### Todo
<div style="font-family: line-height: 1.5em;  myanmar3, padauk, 'noto sans myanmar', pyidaungsu, 'myanmar text'">
* မှတ်တိုင်အလိုက် အချက်အလက်များတွင် ဦးတည်ရာအညွှန်း (သို့) လမ်း၏ မည်သည့်ဘက်တွင် တည်ရှိသည်ကို ထည့်သွင်းသင့်သည်။
</div>

## Note
<div style="font-family: line-height: 1.5em;  myanmar3, padauk, 'noto sans myanmar', pyidaungsu, 'myanmar text'">
မှတ်တိုင်အလိုက် ဖြတ်သန်းသွားသည့် ယာဉ်လိုင်းများ ဖော်ပြရာတွင်၊ တည်နေရာတူညီသည် အခြားမှတ်တိုင်များသို့ ရောက်ရှိသည့် ယာဉ်လိုင်းများအားလည်း တွဲဖက်ပေးထားသည်။ <code>lines-of-bus-stops.js</code> တွင်လေ့လာပါ။

<img src="http://i.imgur.com/AITZoYo.png">

ဥပမာ - မြို့ထဲသို့သွားသည့် "သီတာလမ်း" မှတ်တိုင်နှင့် လမ်းတစ်ဘက်ခြမ်းရှိ တာမွေသို့သွားသည့် "သီတာလမ်း" မှတ်တိုင်တို့သည် မှတ်တိုင်အမှတ် ကွဲပြားသော်လည်း တည်နေရာ တစ်ခုတည်းဖြစ်သည်ဟု မှတ်ယူခြင်းဖြစ်ပါသည်။
</div>

## Disclaimer
<div style="font-family: line-height: 1.5em;  myanmar3, padauk, 'noto sans myanmar', pyidaungsu, 'myanmar text'">
ဤအချက်အလက်များသည် ရန်ကုန်တိုင်းဒေသကြီး အများပြည်သူ သယ်ယူပို့ဆောင်ရေးကြီးကြပ်မှု အာဏာပိုင်အဖွဲ့ (YRTA) တရားဝင် စီမံထိမ်းသိမ်း၍ ဖြန့်ဖြူးထားခြင်း <b>မဟုတ်ပါ</b>။ အချက်အလက် တိကျမှုအားလည်ကောင်း၊ ပြည့်စုံမှုအားလည်ကောင်း အာမမခံပါ။
</div>

## License
<div style="font-family: line-height: 1.5em;  myanmar3, padauk, 'noto sans myanmar', pyidaungsu, 'myanmar text'">
ဤအချက်အလက်များအား YRTA Open Data License 1.0 ပါ ခွင့်ပြုချက်နှင့်အညီ ပြင်ဆင်၍ ပြန်လည်ဖြန့်ဝေသည်။ ဤအချက်အလက်များအား YRTA Open Data License 1.0 ပါ ခွင့်ပြုချက်များ၊ ကန့်သန့်ချက်များနှင့်အညီ ရယူခြင်း၊ ပြင်ဆင်ခြင်း၊ ဖြန့်ဝေခြင်းများ ပြုလုပ်နိုင်သည်။
</div><br><br>
http://data.yangonbus.com/license.html

## Remark
<small>Missing Bus Stop #200 in original source.</small>
