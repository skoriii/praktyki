#plik BED
awk 'BEGIN{OFS="\t"} NR>1 {print "chr"$2, $3, $3+1, $4}' DE_annotated_v2.txt > annotated_v2.bed
#usuwanie redundancji
sort annotated_v2.bed | uniq > annotated_v2_unique.bed


