# Golden Thai Lottery & 2D — Interface Preservation Plan

## Design Objective

ဤပြင်ဆင်မှုတွင် app interface အသစ်ပြန်တည်ဆောက်ခြင်းမဟုတ်ဘဲ လက်ရှိအသုံးပြုနေသော **crown-and-2D visual identity**၊ မြန်မာဘာသာအကြောင်းအရာ၊ mobile portrait layout နှင့် လက်တစ်ဖက်ဖြင့်အသုံးပြုနိုင်သော navigation ကို ထိန်းသိမ်းရန်ဖြစ်သည်။ Error ပြင်ဆင်မှုကြောင့် screen hierarchy၊ အရောင်၊ icon၊ content order သို့မဟုတ် user flow မပြောင်းစေရ။

## Screen List and Primary Content

| Screen | Primary Content and Functionality | Preservation Requirement |
|---|---|---|
| Home | လက်ရှိထီ/2D အချက်အလက်များ၊ အဓိက navigation နှင့် current result cards | Crown-and-2D branding နှင့် မူလအချက်အလက်အစီအစဉ်ကို မပြောင်းရန် |
| Myanmar 2D | 12:01 PM နှင့် 4:30 PM verified results၊ pending ဖြစ်လျှင် dash ပြရန် | မအလုပ်လုပ်သော live SET/VAL/status display မထည့်ရန် |
| 3D Calendar | 2026 ရလဒ်များကို chronological row order ဖြင့်ပြရန် | မူလ row 01 ကို overwrite မလုပ်ရန် |
| Chat | Header ရှိ chat icon နှင့် မြင်သာသော “Chat” label | လက်ရှိ navigation flow ကိုထိန်းသိမ်းရန် |
| Settings/Admin-related Screens | ရှိပြီးသား setting သို့မဟုတ် owner controls | Sole owner-admin identity နှင့် permissions မပြောင်းရန် |

## Key User Flows

အသုံးပြုသူသည် Home မှ သက်ဆိုင်ရာ result section ကိုနှိပ်ပြီး detail screen သို့ဝင်ရောက်ကာ result ကိုကြည့်နိုင်ရမည်။ Back navigation ဖြင့် မူလနေရာသို့ error မရှိဘဲ ပြန်ရမည်။ Chat icon/label ကိုနှိပ်လျှင် လက်ရှိ chat flow သို့ရောက်ရမည်။ Loading သို့မဟုတ် result မရသေးသည့်အခြေအနေတွင် မမှန်သော mock data မပြဘဲ မူလ pending state ကိုသာ ပြရမည်။

## Color and Layout Preservation

လက်ရှိ source archive ထဲရှိ brand colors၊ crown icon၊ 2D icon နှင့် typography ကို source of truth အဖြစ်အသုံးပြုမည်။ Layout သည် **9:16 portrait orientation**၊ safe-area aware spacing၊ one-handed reach နှင့် mainstream iOS interaction pattern ကို ထိန်းသိမ်းရမည်။ Error ပြင်ဆင်ရန်မလိုအပ်သရွေ့ color token သို့မဟုတ် visual asset မပြောင်းရ။

## Scope Guardrail

ဤအဆင့်တွင် feature အသစ်၊ redesign၊ package rename၊ app replacement သို့မဟုတ် data model migration မလုပ်ရ။ Build၊ dependency၊ type နှင့် runtime error များကိုသာ အနည်းဆုံးပြင်ဆင်ချက်ဖြင့် ဖြေရှင်းမည်။
