#feraoun  immunologie 13.12.2025
#Bendellaa sara
# Ouadah khawla 
# Benhamed zohor 
# Benzeghadi saliha
# Derfouf sihem 

import pandas as pd 

#Données :sequence ADN,Longeur,pourcentage de GC 
data ={
"sequence":["ATGCGTACGTA","GCTAGCTAGGCC","ATGCGCGTAAGA","TACGATCGTA","ATGAAAGGCTT","CGTACGTAGC","TTAACCGGAT"],
"Longeur":[12,12,12,10,11,10,10],
"pourcentage GC":[50, 66.67, 58.33, 40, 45.45, 60, 60]
}
#creation D'un DataFrame (tableau pandas)
df=pd.DataFrame(data)
print("*****creation et affichage*****")
print(df) 

#Affichage de tableau 
print ("operation ") 
print("colonne Longeur")
#selectioneer la colonne "Longeur"
Longeur=df["Longeur"] 
print(Longeur)
