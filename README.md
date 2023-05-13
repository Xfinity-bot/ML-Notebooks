# ML-Notebooks

##Use K Means clustering algorithm to divide the following data into two clusters
|x1 | 1 | 2 | 2 | 3 | 4 | 5 |
| - | - | - | - | - | - | - |
|x2 | 1 | 1 | 3 | 2 | 3 | 5 |

K=2

Euclidean distance = Root((x2-x1)^2 + (y2-y1)^2)
(1,1) (2,1)
(1-2)^2

v1 =(2,1) v2=(2,3)

|Data point|Distrance from v1(2,1)| Distance from v2(2,3) | Assigned center|
| - | - | - | -|
|a1 (1,1)| 1 | 2.24 | v1 |
| - | - | - | - |
|a2 (2,1)| 0 | 2 | v1 |
| - | - | - | -|
|a3 (2,3)| 2 | 0 | v2 |
| - | - | - | -|
|a4 (3,2)|  1.41| 1.41 | v1 |
| - | - | - | -|
|a5 (4,3)| 2.83 |2  | v2 |
| - | - | - | -|
|a6 (5,5)| 5 | 3.61 | v2 |

cluster 1 of v1 : { a1,a2,a4 }
cluster 2 of v2 : { a3, a5, a6 }
`v1 =   1/3[(1,1)+(2,1)+(3,2)] = 1/3( 6,4) = (2,1.33)`
`v2 =   1/3[(2,3)+(4,3)+(5,5)] = 1/3(11/11) = (3.67,3.67)`

Step 5 repeat from step 2 until we get same clsuter center or same cluster elements as in the previous iteration

|Data point|Distrance from v1(2,1.33)| Distance from v2(3.67,3.67) | Assigned center |
| - | - | - | -|
|a1 (1,1)| 1.05 | 3.78 | v1 |
| - | - | - | - |
|a2 (2,1)| 0.33 | 3.15 | v1 |
| - | - | - | -|
|a3 (2,3)| 1.67 | 1.8 | v1 |
| - | - | - | -|
|a4 (3,2)|  1.204 | 1.8 | v1 |
| - | - | - | -|
|a5 (4,3)| 2.605 | 0.75  | v2 |
| - | - | - | -|
|a6 (5,5)| 4.74 | 1.88 | v2 |

cluster 1 of v1 = { a1 , a2, a3, a4 }
cluster 2 of v2 = { a5 , a6 }

Recalculatine the cluster centers
 v1 = 1/4 [ a1 + a2 + a3 + a4 ]
      = 1/4 [(1,1)+(2,1)+(2,3)+(3,2)]
      = 1/4[(8,7)] = (2,1.75) 


  v2 = 1/2 [a5+a6]
      = 1/2 [ (4,3) + (5,5)]
      =1/2(9,8) = (4.5,4)  

|Data point|Distrance from v1(2,1.75)| Distance from v2(4.5,4) | Assigned center |
| - | - | - | -|
|a1 (1,1)| 1.25 | 4.61 | v1 |
| - | - | - | - |
|a2 (2,1)| 0.33 | 3.9 | v1 |
| - | - | - | -|
|a3 (2,3)| 1.25 | 2.69 | v1 |
| - | - | - | -|
|a4 (3,2)|  1.03 | 2.5 | v1 |
| - | - | - | -|
|a5 (4,3)| 2.36 | 1.12  | v2 |
| - | - | - | -|
|a6 (5,5)| 4.42 | 1.12 | v2 |

cluster 1 of v1 = { a1 , a2, a3, a4 }
cluster 2 of v2 = { a5 , a6 }

same as in previous iteration 

-----------END------------
