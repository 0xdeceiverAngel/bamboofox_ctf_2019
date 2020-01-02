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