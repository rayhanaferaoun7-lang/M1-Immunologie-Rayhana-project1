#feraoun  immunologie 13.12.2025
#Bendellaa sara,

#ouadah khawla,

#benhamed zohor,

#benzeghadi saliha,

#derfouf sihem

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


#3)filtrage les sequences dont la longeur est superieur à 10

print("filtrage des séquences dont la longeur est superieure à 10")

#filtrer les séquence dont la longeur est superieur à 10

filtred_df = df[df["longeur"]>10]

print(filtred_df)

#4)calculer la moyenne du pourcentage de GC

print("**** calcul de la moyenne ****")

# calcule la moyenne du pourcentage de GC

average_gc=df["pourcentage GC"].mean()

print(f"poucentage moyen de GC:{average_gc:.3f}%

#5)Ajouter une nouvelle colonne

print("******ajoute d'une nouvelle colonne******")

# Ajouter une nouvelle colonne "catégorie GC"

df["catégorie GC"] = df["pourcentage GC"].apply(lambda x:"Riche"if x>55 else ("moyen"if x>=45else "Faible" ))

print(df) 

#6)Ajouter une colonne comptant les "G"
df["Nombre de G"]= df["sequence"].str.count("G")
print("****Nombre de G ajoutés****")
print(df,"\n")






