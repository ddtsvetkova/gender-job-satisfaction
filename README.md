# Who is more satisfied at work: women or men? Gender differences in job satisfaction in Russia.


```stata

* Working with the data set on individuals
use "INSERT YOUR PATH HERE\USER_RLMS-HSE_IND_1994_2020_v4_rus.dta"

keep origsm inwgt ID_I ID_H ID_W idind year INT_Y OCCUP08 REDID_I region marst diplom age H5 J1_1_1 J1_1_2 J1_1_3 J1_1_4 J1 J2COD08 J4_1 J6 I4 J8 J8_1 J13 J13_2 J26 J29C_1 J29C_2 J22 J31 J32 J72_173 M3 J10 J29_2_1 J29_2_3 J60_5A J62 J11 J11_1 J21_3 J23 J5A J5B J60 H7_2 J29 J61

describe

tabulate year
tabulate ID_W
keep if year >= 2016
tabulate year

* save "INSERT YOUR PATH HERE\new_ind.dta"

use "INSERT YOUR PATH HERE\USER_RLMS-HSE_HH_1994_2020_rus.dta", clear

keep ID_W REDID_H ID_H origsam hhwgt C1 F14 F9_11_1 F9_11_2 F9_11_3 F9_11_4 F9_11_5

describe

tab ID_W, nolabel
keep if ID_W >= 25
tab ID_W, nolabel

* save "D:\Dasha's\HSE\3 курс\Курсовая\new_hh.dta", replace

* use "D:\Dasha's\HSE\3 курс\Курсовая\new_ind.dta", clear
```{:.language-stata}

```r
X %>% dplyr::mutate()
```
