
#### *Marcus W. Beck, marcusb@sccwrp.org, Raphael D. Mazor, raphaelm@sccwrp.org, Mark Engeln*

# PHABMetrics

[![Travis-CI Build Status](https://travis-ci.org/SCCWRP/PHABMetrics.svg?branch=master)](https://travis-ci.org/SCCWRP/PHABMetrics)
[![AppVeyor Build Status](https://ci.appveyor.com/api/projects/status/github/SCCWRP/PHABMetrics?branch=master&svg=true)](https://ci.appveyor.com/project/SCCWRP/PHABMetrics)

This package provides functions to calculate PHAB metrics using field data.

# Installing the package

The development version of this package can be installed from Github:


```r
install.packages('devtools')
library(devtools)
install_github('SCCWRP/PHABMetrics')
library(PHABMetrics)
```

# Usage

The core  function is `phabmetrics()`.



```r
alldat <- phabmetrics(sampdat)
alldat
```

```
##           StationCode CFC_ALG.result CFC_ALL_EMAP.result
## 1 402M00002_8/13/2015             11                   6
## 2  SMC00710_5/20/2009             22                   5
## 3  SMC00957_6/21/2010             77                   7
## 4   SMC04383_6/9/2010              2                   7
##   CFC_ALL_SWAMP.result CFC_AQM.result CFC_BRS.result CFC_HUM.result
## 1                    7             11             11              0
## 2                    6             20             22              0
## 3                    8             56             77             14
## 4                    8             16              6              4
##   CFC_LTR.result CFC_LWD.result CFC_OHV.result CFC_RCK.result
## 1             11              0             11             11
## 2             20              0             22             22
## 3             77              7             77              0
## 4              2              8             16              0
##   CFC_UCB.result Ev_AqHab.count Ev_AqHab.result Ev_FlowHab.result
## 1             11              7       0.9195058         0.7394590
## 2              0              8       0.7011374         0.8901335
## 3             70              8       0.6239169         0.5132618
## 4              2              6       0.7003733         0.6979406
##   Ev_SubNat.result  FL_F.result FL_M.result FL_N_F.result FL_N_M.result
## 1                0  2.855641769  0.08086277            NA            NA
## 2                0  0.000000000  0.00000000            NA            NA
## 3                0  0.002344635  0.08280000   0.002344635        0.0828
## 4                0 14.754146820  0.41779091            NA            NA
##   FL_Q_F.result FL_Q_M.result H_AqHab.count H_AqHab.result H_FlowHab.count
## 1      2.855642    0.08086277             7       1.789276               3
## 2      0.000000    0.00000000             8       1.457974               3
## 3            NA            NA             8       1.297399               5
## 4     14.754147    0.41779091             6       1.254901               4
##   H_FlowHab.result H_SubNat.count H_SubNat.result MWVM_F.result
## 1        0.8123787              0               0          2.29
## 2        0.9779116              0               0          0.58
## 3        0.8260630              0               0          1.00
## 4        0.9675511              0               0          0.88
##   MWVM_M.result NFC_DLU.result NFC_EFR.result NFC_ERN.result PBM_E.result
## 1      0.697992          Other             NO             NO     13.63636
## 2      0.176784 Suburban, Town             NO             NO     40.66667
## 3      0.304800 Suburban, Town             NO             NO     36.36364
## 4      0.268224         Forest             NO             NO      0.00000
##   PBM_S.result PBM_V.result PCT_BDRK.result PCT_BIGR.result PCT_CB.result
## 1     4.545455     81.81818               0        27.83505      11.34021
## 2     0.000000     59.33333               0        72.44094      32.28346
## 3    45.454545     18.18182               0         0.00000       0.00000
## 4   100.000000      0.00000               0        56.19048      16.19048
##   PCT_CF.count PCT_CF.result PCT_CF.sd PCT_CF_WT.count PCT_CF_WT.result
## 1           10           0.0 0.0000000              10                0
## 2           70           0.0 0.0000000              70                0
## 3           20           0.0 0.0000000              20                0
## 4           20           1.5 0.3077935              20                3
##   PCT_CPOM.result PCT_DR.count PCT_DR.result PCT_DR.sd PCT_FAST.result
## 1        20.61856           10             0         0             4.0
## 2        56.69291           70             0         0            31.5
## 3        48.57143           20             0         0            15.5
## 4        26.66667           20             0         0            76.5
##   PCT_FAST_WT.result PCT_FN.result PCT_GC.result PCT_GF.result
## 1                4.0     35.051546      9.278351      4.123711
## 2              220.5      0.000000     39.370079     10.236220
## 3               31.0      0.000000      0.000000     21.904762
## 4              153.0      1.904762     13.333333     28.571429
##   PCT_GL.count PCT_GL.result PCT_GL.sd PCT_GL_WT.count PCT_GL_WT.result
## 1           10            38  4.817791              10               38
## 2           70            64  3.947481              70              448
## 3           20            55  6.190825              20              110
## 4           20            19  3.079645              20               38
##   PCT_HP.result PCT_MAA.result PCT_MAP.result PCT_MAU.result
## 1             0        2.12766        2.12766       0.000000
## 2             0       69.60000       69.60000       0.000000
## 3             0       10.47619       11.42857       0.952381
## 4             0       36.36364       39.39394       4.040404
##   PCT_MCP.result PCT_MIAT1.result PCT_MIAT1P.result PCT_MIATP.result
## 1      13.829787         3.260870         75.000000         4.347826
## 2       3.937008         0.000000          0.000000        86.842105
## 3      39.047619         0.952381          2.222222        42.857143
## 4       0.000000         0.000000          0.000000        38.775510
##   PCT_NSA.result PCT_OT.result PCT_POOL.count PCT_POOL.result PCT_POOL.sd
## 1       5.319149     19.587629             10            58.0    3.653005
## 2      69.600000      2.362205             70             4.5    1.410108
## 3      12.380952      0.000000             20            29.5    4.459172
## 4      39.795918      0.000000             20             4.5    1.436370
##   PCT_POOL_WT.count PCT_POOL_WT.result PCT_RA.count PCT_RA.result
## 1                10               58.0           10             0
## 2                70               31.5           70             0
## 3                20               59.0           20             0
## 4                20                9.0           20             0
##   PCT_RA.sd PCT_RA_WT.count PCT_RA_WT.result PCT_RC.result PCT_RI.count
## 1         0              10                0             0           10
## 2         0              70                0             0           70
## 3         0              20                0             0           20
## 4         0              20                0             0           20
##   PCT_RI.result PCT_RI.sd PCT_RI_WT.count PCT_RI_WT.result PCT_RN.count
## 1           4.0 0.9660918              10              4.0           10
## 2          23.5 2.2273010              70            164.5           70
## 3           0.0 0.0000000              20              0.0           20
## 4          73.0 2.5567249              20            146.0           20
##   PCT_RN.result PCT_RN.sd PCT_RN_WT.count PCT_RN_WT.result PCT_RR.result
## 1           0.0  0.000000              10                0             0
## 2           8.0  2.526096              70               56             0
## 3          15.5  1.450953              20               31             0
## 4           2.0  2.430075              20                4             0
##   PCT_RS.result PCT_SA.result PCT_SAFN.result PCT_SB.result
## 1             0      9.278351        44.32990     7.2164948
## 2             0     14.960630        14.96063     0.7874016
## 3             0     78.095238        78.09524     0.0000000
## 4             0     13.333333        15.23810    20.0000000
##   PCT_SFGF.result PCT_SLOW.result PCT_SLOW_WT.result PCT_WD.result
## 1        48.45361            96.0               96.0      4.123711
## 2        25.19685            68.5              479.5      0.000000
## 3       100.00000            84.5              169.0      0.000000
## 4        43.80952            23.5               47.0      0.000000
##   PCT_XB.result PWVZ.result RBP_CHN.result RBP_EPI.result RBP_SED.result
## 1      0.000000    45.45455             NA             NA             NA
## 2      0.000000    15.78947             19             14             17
## 3      0.000000     0.00000             NA             NA             NA
## 4      6.666667     0.00000             17             17             18
##   SB_PP_D10.result SB_PP_D25.result SB_PP_D50.result SB_PP_D75.result
## 1             0.03             0.03             1.03            40.00
## 2             1.03             9.00            40.00           157.00
## 3             1.03             1.03             1.03             1.03
## 4             1.03             9.00            40.00           625.00
##   SB_PP_D90.result SB_PT_D10.result SB_PT_D25.result SB_PT_D50.result
## 1              157             0.03             0.03             1.03
## 2              157             1.03             9.00            40.00
## 3                9             1.03             1.03             1.03
## 4              625             1.03             9.00            40.00
##   SB_PT_D75.result SB_PT_D90.result SINU.NOT_WORKING SLOPE_0.count
## 1            40.00              157         28.64934            10
## 2           157.00              157         31.83260            10
## 3             1.03                9         28.64934            10
## 4           625.00              625         28.64934            10
##   SLOPE_0.result SLOPE_0_5.count SLOPE_0_5.result SLOPE_1.count
## 1         0.0000              10         666.6667            10
## 2       666.6667              10           0.0000            10
## 3       666.6667              10           0.0000            10
## 4       666.6667              10           0.0000            10
##   SLOPE_1.result SLOPE_2.count SLOPE_2.result W1_HALL_EMAP.result
## 1       666.6667            10       666.6667                   4
## 2         0.0000            10         0.0000                   8
## 3         0.0000            10         0.0000                  28
## 4         0.0000            10         0.0000                   8
##   W1_HALL_SWAMP.result W1H_BLDG.count W1H_BLDG.result W1H_BLDG.sd
## 1                    4             11               1           0
## 2                    8             11               2           0
## 3                   28             11               7           0
## 4                    8             11               2           0
##   W1H_BRDG.count W1H_BRDG.result W1H_BRDG.sd W1H_CROP.count
## 1             11               1           0             11
## 2             11               2           0             11
## 3             11               7           0             11
## 4             11               2           0             11
##   W1H_CROP.result W1H_CROP.sd W1H_LDFL.count W1H_LDFL.result W1H_LDFL.sd
## 1               1           0             11               1           0
## 2               2           0             11               2           0
## 3               7           0             11               7           0
## 4               2           0             11               2           0
##   W1H_LOG.count W1H_LOG.result W1H_LOG.sd W1H_MINE.count W1H_MINE.result
## 1            11              1          0             11               1
## 2            11              2          0             11               2
## 3            11              7          0             11               7
## 4            11              2          0             11               2
##   W1H_MINE.sd W1H_ORVY.count W1H_ORVY.result W1H_ORVY.sd W1H_PARK.count
## 1           0             11               1           0             11
## 2           0             11               2           0             11
## 3           0             11               7           0             11
## 4           0             11               2           0             11
##   W1H_PARK.result W1H_PARK.sd W1H_PIPE.count W1H_PIPE.result W1H_PIPE.sd
## 1               1           0             11               1           0
## 2               2           0             11               2           0
## 3               7           0             11               7           0
## 4               2           0             11               2           0
##   W1H_PSTR.count W1H_PSTR.result W1H_PSTR.sd W1H_PVMT.count
## 1             11               1           0             11
## 2             11               2           0             11
## 3             11               7           0             11
## 4             11               2           0             11
##   W1H_PVMT.result W1H_PVMT.sd W1H_ROAD.count W1H_ROAD.result W1H_ROAD.sd
## 1               1           0             11               1           0
## 2               2           0             11               2           0
## 3               7           0             11               7           0
## 4               2           0             11               2           0
##   W1H_VEGM.count W1H_VEGM.result W1H_VEGM.sd W1H_WALL.count
## 1             11               1           0             11
## 2             11               2           0             11
## 3             11               7           0             11
## 4             11               2           0             11
##   W1H_WALL.result W1H_WALL.sd XBEARING.count XBEARING.result XBEARING.sd
## 1               1           0             11     0.009090909 0.003015113
## 2               2           0             12     0.007500000 0.004522670
## 3               7           0             11     0.009090909 0.003015113
## 4               2           0             11     0.009090909 0.003015113
##   XBKF_H.count XBKF_H.result XBKF_H.sd XBKF_W.count XBKF_W.result
## 1           11     0.6590909 0.0202260           11     15.545455
## 2           77     0.4918182 0.7186184           77      6.130909
## 3           22     0.3581818 0.1206189           22      3.029091
## 4           22     0.8645455 0.1197111           22     18.681818
##   XBKF_W.sd XC.count XC.result    XC.sd XCDENBK.count XCDENBK.result
## 1 2.8762349       22  15.11364 14.06781             0             NA
## 2 1.7371500       22  58.75000 25.11580             0             NA
## 3 0.8329232       22  20.68182 24.53353             0             NA
## 4 5.4864019       22  28.97727 21.65282             0             NA
##   XCDENBK.sd XCDENMID.count XCDENMID.result XCDENMID.sd XCM.result
## 1         NA             44        77.00535    35.08415   56.36364
## 2         NA             88        84.75936    18.59386  117.38636
## 3         NA             44        53.87701    34.32184   43.86364
## 4         NA             44        50.00000    35.09978   51.13636
##   XCMG.result XEMBED.count XEMBED.result XEMBED.sd XFC_ALG.count
## 1    80.90909           12      45.41667  30.70818            11
## 2   155.45455           41      13.29268  11.04591            22
## 3    69.09091            0            NA        NA            77
## 4    95.34091           14      44.28571  28.00118            22
##   XFC_ALG.result XFC_ALG.sd XFC_AQM.count XFC_AQM.result XFC_AQM.sd
## 1     12.2727273  10.090500            11      22.954545  23.500484
## 2     22.5000000  14.433757            22       4.545455   1.471225
## 3     84.7727273   8.680948            77       3.636364   2.241411
## 4      0.4545455   1.471225            22      32.954545  35.670753
##   XFC_BIG.result XFC_BRS.count XFC_BRS.result XFC_BRS.sd XFC_HUM.count
## 1      32.500000            11      14.090909   10.44466            11
## 2      62.500000            22       5.000000    0.00000            22
## 3      22.727273            77       5.000000    0.00000            77
## 4       6.818182            22       3.181818    7.32664            22
##   XFC_HUM.result XFC_HUM.sd XFC_LTR.count XFC_LTR.result XFC_LTR.sd
## 1      0.0000000   0.000000            11      10.454545   9.341987
## 2      0.0000000   0.000000            22       4.545455   1.471225
## 3      5.6818182  16.556504            77      20.681818  15.025397
## 4      0.9090909   1.973855            22       2.272727   7.356124
##   XFC_LWD.count XFC_LWD.result XFC_LWD.sd XFC_NAT_EMAP.result
## 1            11      0.0000000   0.000000            83.40909
## 2            22      0.0000000   0.000000            76.13636
## 3            77      0.4545455   1.446825            50.45455
## 4            22      5.4545455   9.625004            32.50000
##   XFC_NAT_SWAMP.result XFC_OHV.count XFC_OHV.result XFC_OHV.sd
## 1            116.81818            11      36.818182   16.39706
## 2             85.22727            22       8.636364    7.89542
## 3             74.77273            77      28.409091   19.76386
## 4             67.72727            22      23.409091   23.53500
##   XFC_RCK.count XFC_RCK.result XFC_RCK.sd XFC_UCB.count XFC_UCB.result
## 1            11           27.5   28.19574            11      5.0000000
## 2            22           62.5   22.75647            22      0.0000000
## 3            77            0.0    0.00000            77     16.5909091
## 4            22            0.0    0.00000            22      0.4545455
##   XFC_UCB.sd XG.result XGB.count XGB.result   XGB.sd XGH.count XGH.result
## 1   0.000000  24.54545        22   82.04545 11.84313        22   19.54545
## 2   0.000000  38.06818        22   14.88636 14.27780        22   12.27273
## 3  16.352959  25.22727        22   20.34091 34.86620        22   20.90909
## 4   1.471225  44.20455        22   33.86364 14.81487        22   21.02273
##      XGH.sd XGW.count XGW.result    XGW.sd XM.count XM.result    XM.sd
## 1  9.116846        22   5.000000  0.000000       22  41.25000 16.63241
## 2  9.847319        22  25.795455 15.047274       22  58.63636 26.91175
## 3 26.865466        22   4.318182  8.632091       22  23.18182 23.74445
## 4 12.165992        22  23.181818  5.884899       22  22.15909 17.17029
##   XMIAT.count XMIAT.result  XMIAT.sd XMIATP.count XMIATP.result XMIATP.sd
## 1          92    0.1032609 0.5372807            4     2.3750000 1.2500000
## 2         114    0.3245614 0.1725967           99     0.3737374 0.1256297
## 3         105    0.1666667 0.3319281           45     0.3888889 0.4147684
## 4          98    0.1173469 0.1613573           38     0.3026316 0.1032887
##   XPCAN.result XPCM.result XPCMG.result XPGVEG.result XPMGVEG.result
## 1    0.9090909           1            1             1              0
## 2    1.0000000           1            1             1              0
## 3    0.6818182           1            1             1              0
## 4    1.0000000           1            1             1              0
##   XPMID.result XSDGM.result XSLOPE.count XSLOPE.result   XSLOPE.sd
## 1     1.000000     1.377776           11   0.009090909 0.003015113
## 2     1.000000    31.377005           12   0.000000000 0.000000000
## 3     1.466667     1.655960           11   0.000000000 0.000000000
## 4     1.000000    39.827686           11   0.000000000 0.000000000
##   XSPGM.result XWAK.result XWDA.count XWDA.result XWDEPTH.count
## 1     1.377776         341         97   0.3629066            97
## 2    31.377005         198        735   0.2432594           735
## 3     1.655960         200        240   0.3511581           240
## 4    39.827686         310        210   0.1377978           210
##   XWDEPTH.result XWDEPTH.sd XWDM.count XWDM.result XWDO.result XWDR.count
## 1      33.845361   24.49036         17    60.17647        3.90         21
## 2       7.733333   20.43468         42    14.21429        8.86        147
## 3       5.116667   22.07518         21     9.47619        7.19         48
## 4      14.600000   18.81383         21    31.09524        9.70         42
##   XWDR.result XWIDTH.count XWIDTH.result XWIDTH.sd XWPH.result XWSC.result
## 1    27.55530           21      9.326190 16.252179        7.62    1806.000
## 2    41.10837          147      3.179048 17.316949        7.91     764.000
## 3    28.47720           48      1.457083  8.350054        7.57    1985.474
## 4    72.57012           42     10.595238 16.582599        8.51    1188.000
##   XWSL.result XWTB.result XWTC.result XWTF.result XWV_F.result
## 1        0.92          NA       20.50      68.900    0.5009091
## 2        0.45        10.8       16.22      61.196    0.1973684
## 3        1.20          NA       18.68      65.624    1.0000000
## 4        0.60          NA       20.90      69.620    0.2287500
##   XWV_M.result
## 1   0.15267709
## 2   0.06015789
## 3   0.30480000
## 4   0.06972300
```



The following 161 metrics are calculated:

```
##   [1] "CFC_ALG"       "CFC_ALL_EMAP"  "CFC_ALL_SWAMP" "CFC_AQM"      
##   [5] "CFC_BRS"       "CFC_HUM"       "CFC_LTR"       "CFC_LWD"      
##   [9] "CFC_OHV"       "CFC_RCK"       "CFC_UCB"       "Ev_AqHab"     
##  [13] "Ev_FlowHab"    "Ev_SubNat"     "FL_F"          "FL_M"         
##  [17] "FL_N_F"        "FL_N_M"        "FL_Q_F"        "FL_Q_M"       
##  [21] "H_AqHab"       "H_FlowHab"     "H_SubNat"      "MWVM_F"       
##  [25] "MWVM_M"        "NFC_DLU"       "NFC_EFR"       "NFC_ERN"      
##  [29] "PBM_E"         "PBM_S"         "PBM_V"         "PCT_BDRK"     
##  [33] "PCT_BIGR"      "PCT_CB"        "PCT_CF"        "PCT_CF_WT"    
##  [37] "PCT_CPOM"      "PCT_DR"        "PCT_FAST"      "PCT_FAST_WT"  
##  [41] "PCT_FN"        "PCT_GC"        "PCT_GF"        "PCT_GL"       
##  [45] "PCT_GL_WT"     "PCT_HP"        "PCT_MAA"       "PCT_MAP"      
##  [49] "PCT_MAU"       "PCT_MCP"       "PCT_MIAT1"     "PCT_MIAT1P"   
##  [53] "PCT_MIATP"     "PCT_NSA"       "PCT_OT"        "PCT_POOL"     
##  [57] "PCT_POOL_WT"   "PCT_RA"        "PCT_RA_WT"     "PCT_RC"       
##  [61] "PCT_RI"        "PCT_RI_WT"     "PCT_RN"        "PCT_RN_WT"    
##  [65] "PCT_RR"        "PCT_RS"        "PCT_SA"        "PCT_SAFN"     
##  [69] "PCT_SB"        "PCT_SFGF"      "PCT_SLOW"      "PCT_SLOW_WT"  
##  [73] "PCT_WD"        "PCT_XB"        "PWVZ"          "RBP_CHN"      
##  [77] "RBP_EPI"       "RBP_SED"       "SB_PP_D10"     "SB_PP_D25"    
##  [81] "SB_PP_D50"     "SB_PP_D75"     "SB_PP_D90"     "SB_PT_D10"    
##  [85] "SB_PT_D25"     "SB_PT_D50"     "SB_PT_D75"     "SB_PT_D90"    
##  [89] "SINU"          "SLOPE_0"       "SLOPE_0_5"     "SLOPE_1"      
##  [93] "SLOPE_2"       "W1_HALL_EMAP"  "W1_HALL_SWAMP" "W1H_BLDG"     
##  [97] "W1H_BRDG"      "W1H_CROP"      "W1H_LDFL"      "W1H_LOG"      
## [101] "W1H_MINE"      "W1H_ORVY"      "W1H_PARK"      "W1H_PIPE"     
## [105] "W1H_PSTR"      "W1H_PVMT"      "W1H_ROAD"      "W1H_VEGM"     
## [109] "W1H_WALL"      "XBEARING"      "XBKF_H"        "XBKF_W"       
## [113] "XC"            "XCDENBK"       "XCDENMID"      "XCM"          
## [117] "XCMG"          "XEMBED"        "XFC_ALG"       "XFC_AQM"      
## [121] "XFC_BIG"       "XFC_BRS"       "XFC_HUM"       "XFC_LTR"      
## [125] "XFC_LWD"       "XFC_NAT_EMAP"  "XFC_NAT_SWAMP" "XFC_OHV"      
## [129] "XFC_RCK"       "XFC_UCB"       "XG"            "XGB"          
## [133] "XGH"           "XGW"           "XM"            "XMIAT"        
## [137] "XMIATP"        "XPCAN"         "XPCM"          "XPCMG"        
## [141] "XPGVEG"        "XPMGVEG"       "XPMID"         "XSDGM"        
## [145] "XSLOPE"        "XSPGM"         "XWAK"          "XWDA"         
## [149] "XWDEPTH"       "XWDM"          "XWDO"          "XWDR"         
## [153] "XWIDTH"        "XWPH"          "XWSC"          "XWSL"         
## [157] "XWTB"          "XWTC"          "XWTF"          "XWV_F"        
## [161] "XWV_M"
```

# Required data checks

* For every function, make sure there are no duplicate or conflicting values for every unique combination of `id`, `LocationCode`, `AnalyteName`, and `VariableResult` (or `Result`).  This should be specific to the metric classes just to be safe.  For example, every combination should have only one entry in `VariableResult` for `AnalyteName %in% c('Microalgae Thickness', 'Macrophyte Cover', 'Macroalgae Cover, Attached', 'Macroalgae Cover, Unattached')` for the algae metrics.  The `algae.R` function will remove duplicate entries but a checker should be built that verifies a unique value can be determined.  

* Required column names, see those in `sampdat`.  

* Check for required values in `AnalyteName` (note that `chkinp()` can check of the columns exist but we'll need a checker on data input to check for these and only these): 
     * `c('Microalgae Thickness', 'Macrophyte Cover', 'Macroalgae Cover, Attached', 'Macroalgae Cover, Unattached')` for `algae()`
     * `c('Bankfull Height', 'Bankfull Width', 'StationWaterDepth', 'Wetted Width')` for `bankmorph()`
     * `c('Cascade/Falls', 'Dry', 'Glide', 'Pool', 'Rapid', 'Riffle', 'Run'))` for `channelmorph()` 
     * `c(Slope', 'Length, Segment', 'Elevation Difference', 'Bearing', 'Proportion', 'Length, Reach')` for `channelsinuosity()`
     * `c('Canopy Cover')` for `densiometer()`
     * `c('Distance from Bank', 'StationWaterDepth', 'Velocity', 'Distance, Float', 'Float Time', 'Wetted Width')` for `flow()`
     * `c('Fish Cover Macrophytes', 'Fish Cover Artificial Structures', 'Fish Cover Boulders', 'Fish Cover Filamentous Algae', 'Fish Cover Woody Debris >0.3 m', 'Fish Cover Live Trees/Roots', 'Fish Cover Overhang.Veg', 'Fish Cover Woody Debris <0.3 m', 'Fish Cover Undercut Banks')` for `habitat()`
     * `c('Riparian Bridges/Abutments', 'Riparian Buildings', 'Riparian Landfill/Trash', 'Riparian Logging', 'Riparian Mining', 'Riparian Orchards/Vineyards', 'Riparian Park/Lawn', 'Riparian Pasture/Range', 'Riparian Pavement', 'Riparian Pipes', 'Riparian Road', 'Riparian Row Crops', 'Riparian Vegetation Management', 'Riparian Wall/Dike')` for `disturbance()`
     * `c('Riffle/Run Channel Alteration', 'Riffle/Run Epifaunal Substrate', 'Riffle/Run Sediment Deposition', 'Dominant Land Use', 'Evidence of Fire', 'Evidence of Recent Rainfall')` for `misc()`
     * `c('Bank Stability')` for `bankstability()`
     * `c("Alkalinity as CaCO3", "Oxygen, Dissolved", "pH", "Salinity", "SpecificConductivity", "Temperature", "Turbidity")` for `quality()`
     * `c('Riparian GroundCover Barren', 'Riparian GroundCover NonWoody Plants', 'Riparian GroundCover Woody Shrubs', 'Riparian Lower Canopy All Vegetation', 'Riparian Upper Canopy All Trees', 'Riparian Lower Canopy All Vegetation', 'Riparian Upper Canopy All Trees', 'Riparian GroundCover Woody Shrubs', 'Riparian GroundCover NonWoody Plants')` for `ripveg()` 
     * `c('Substrate Size Class', 'Embeddedness', 'CPOM')` for `substrate()`
     
* Check for required values in `LocationCode` (note that `chkinp()` can check of the columns exist but we'll need a checker on data input to check for these and only these)

* Maybe we need to add a checker to make sure all values in each field are present but with appropriate NA values for `Result`, `VariableResult`, this can be done with `tidyr::complete()` but may be unnecessary since this will increase data volume 
