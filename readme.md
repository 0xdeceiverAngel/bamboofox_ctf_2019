# bamboofox ctf 019
## How2decompyle
### review
給你檔案，上網de回python，然後就是逆他
### code 
```py
restrictions = [
 'uudcjkllpuqngqwbujnbhobowpx_kdkp_',
 'f_negcqevyxmauuhthijbwhpjbvalnhnm',
 'dsafqqwxaqtstghrfbxzp_x_xo_kzqxck',
 'mdmqs_tfxbwisprcjutkrsogarmijtcls',
 'kvpsbdddqcyuzrgdomvnmlaymnlbegnur',
 'oykgmfa_cmroybxsgwktlzfitgagwxawu',
 'ewxbxogihhmknjcpbymdxqljvsspnvzfv',
 'izjwevjzooutelioqrbggatwkqfcuzwin',
 'xtbifb_vzsilvyjmyqsxdkrrqwyyiu_vb',
 'watartiplxa_ktzn_ouwzndcrfutffyzd',
 'rqzhdgfhdnbpmomakleqfpmxetpwpobgj',
 'qggdzxprwisr_vkkipgftuvhsizlc_pbz',
 'jerzhlnsegcaqzathfpuufwunakdtceqw',
 'lbvlyyrugffgrwo_v_zrqvqszchqrrljq',
 'aiwuuhzbszvfpidwwkl_wynlujbsbhfox',
 'vmhrizxtiegxdxsqcdoiyxkffloudwtxg',
 'tffjnabob_jbf_qiszdsemczghnjysmah',
 'zrqkppvynlkelnevngwlkhgaputhoagtt',
 'nl_oojyafwoqccbedijmigpedkdzglq_f',
 'cksy_skctjlyxktuzchvstunyvcvabomc',
 'ppcxleeguvhvhengmvac_bykhzqohjuei',
 '_clmaicjrrzhwd_fescyaejtbyefxyihy',
 'hhopvwsmjtpjiffzatyhjrev_dwnsidyo',
 'sjevtrmkkk_zjalxrxfovjsbcxjx_pskp',
 'gnynwuuqypddbsylparpcczqimimqmvdl',
 'bxitcmhnmanwuhvjxnqeoiimlegrmkjra']
samp=set('abcdefghijklmnopqrstuvwxyz_')
str=''
# samp=['a','b','c','d','e','f','g','h','i','j','k','l','m','n','o','p','q','r','s','t','u','v','w','x','y','z']
tmp=[]
# tmp=set()
for j in range(33):
    for i in restrictions:
        # tmp.add(i[j])
        # print(i[j])
        tmp.append(i[j])
    str+=''.join(samp-set(tmp))
    tmp.clear()
    # tmp.clear()
print(str)
```
>you_know_decompyle_and_do_reverse

丟回去原本的code，他幫你改大寫
```py
# BAMBOOFOX{we1c0me_t0_B4mbooF0x_CTF}
# BAMBOOFOX{you_know_decompyle_and_do_reverse}

# Python bytecode 2.7 (62211)
# Embedded file name: decompyle.py
# Compiled at: 2019-09-22 20:18:03
# Decompiled by https://python-decompiler.com
import string
restrictions = [
 'uudcjkllpuqngqwbujnbhobowpx_kdkp_',
 'f_negcqevyxmauuhthijbwhpjbvalnhnm',
 'dsafqqwxaqtstghrfbxzp_x_xo_kzqxck',
 'mdmqs_tfxbwisprcjutkrsogarmijtcls',
 'kvpsbdddqcyuzrgdomvnmlaymnlbegnur',
 'oykgmfa_cmroybxsgwktlzfitgagwxawu',
 'ewxbxogihhmknjcpbymdxqljvsspnvzfv',
 'izjwevjzooutelioqrbggatwkqfcuzwin',
 'xtbifb_vzsilvyjmyqsxdkrrqwyyiu_vb',
 'watartiplxa_ktzn_ouwzndcrfutffyzd',
 'rqzhdgfhdnbpmomakleqfpmxetpwpobgj',
 'qggdzxprwisr_vkkipgftuvhsizlc_pbz',
 'jerzhlnsegcaqzathfpuufwunakdtceqw',
 'lbvlyyrugffgrwo_v_zrqvqszchqrrljq',
 'aiwuuhzbszvfpidwwkl_wynlujbsbhfox',
 'vmhrizxtiegxdxsqcdoiyxkffloudwtxg',
 'tffjnabob_jbf_qiszdsemczghnjysmah',
 'zrqkppvynlkelnevngwlkhgaputhoagtt',
 'nl_oojyafwoqccbedijmigpedkdzglq_f',
 'cksy_skctjlyxktuzchvstunyvcvabomc',
 'ppcxleeguvhvhengmvac_bykhzqohjuei',
 '_clmaicjrrzhwd_fescyaejtbyefxyihy',
 'hhopvwsmjtpjiffzatyhjrev_dwnsidyo',
 'sjevtrmkkk_zjalxrxfovjsbcxjx_pskp',
 'gnynwuuqypddbsylparpcczqimimqmvdl',
 'bxitcmhnmanwuhvjxnqeoiimlegrmkjra']
# capital = [
#  0, 4, 9, 19, 23, 26]
# flag = input('Please tell me something : ').lower()
# flag = flag.lower()
# if len(flag) != len(restrictions[0]):
#     # print 'No......You are wrong orzzzzz'
#     # exit(0)
# for f in range(len(flag)):
#     for r in restrictions:
#         if flag[f] not in string.lowercase + '_' or flag[f] == r[f]:
#             # print 'No......You are wrong orzzzzzzzzzzzz'
#             # exit(0)
flag='you_know_decompyle_and_do_reverse'
capital = [
 0, 4, 9, 19, 23, 26]
cap_flag = ''
for f in range(len(flag)):
    if f in capital:
        cap_flag += flag[f].upper()
    else:
        cap_flag += flag[f]

print ('Yeah, you got it !\nBambooFox{' + cap_flag + '}\n')

```
> BambooFox{You_Know_Decompyle_And_Do_Reverse}

## MOVE OR NOT
### review
逆向之後 第一關是 98416 
第二關 爆破比較快 因為他是吃輸入 對 資料做運算 然後call 

### code
```sh
#!/usr/bin/expect
set i 0
for {set key 0} {$key<=255} {incr key} {
    
    spawn  ./pro
    expect "*password: " {send "98416\r"}
    expect "*key: " {send "$key\r"}
    expect "*flag: " { send "Test_flag\r"}
}

```
> ./pro.sh|grep -B 1 'flag'

之後挨個ltrace 測試  會發現50 有過

```
$trace ./pro
printf("First give me your password: ") = 29
__isoc99_scanf(0x555555554a06, 0x7fffffffdf28, 0, 0First give me your password: 98416
) = 1
printf("Second give me your key: ") = 25
__isoc99_scanf(0x555555554a06, 0x7fffffffdf28, 0, 0Second give me your key: 50
) = 1
printf("Then Verify your flag: ") = 23
__isoc99_scanf(0x555555554a63, 0x7fffffffdf30, 0, 0Then Verify your flag: 5
) = 1
strcmp("BambooFox{dyn4mic_1s_4ls0_gr34t}"..., "5") = 13
puts("You don't know dynamic analysis "...You don't know dynamic analysis !
) = 34
+++ exited (status 0) +++
```
>  BambooFox{dyn4mic_1s_4ls0_gr34t}
