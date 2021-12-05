# Automated Waste Classification with CNNs in Realistic Contexts 

Here I will keep track of progresses in this project in which I'm trying to model a CNN capable of distinguish different categories of wastes from images and photos taken in different contexts and with various backgrounds. 

# Little bit of backstory 

I started this project for my bachelor's degree thesis in September 2020 and I'm still working on it to obtain better results.  
Let's get rid of all that trash, or better, let's recycle! 

# Come leggere i nomi dei file

## DATASET

(ds, split o test)_(Immagini)_(Numero classi)

ds_** : cartelle dei dataset destinati al train/val/test o solo train/val, categorie
split_**: dataset già splittati in train/val/test, ognuno diviso nelle categorie
png_**: immagini cleaned senza background, divisi nelle categorie
test_**: testset diviso in categorie

### Immagini
- "clean": contengono le immagini della size adatta ai modelli, divise per categorie
- "realistic": creato da me
- "newBG": con background aumentato
- "C+BG": clean + newBG

### Numero classi
-"6": 6 categorie (cardboard, glass, paper, metal, plastic, trash), usato nel modello A
-"7": 7 categorie (stesse + compost)


## MODELS
model_(Modello)_(Training set usato).h5

### Modelli

A: modello basato su AlexNet (7 classi)

B: modello basato su Inception ResNet v4 (7 classi)

### Training set usato

C: cleaned, training fatto su immagini con sfondo neutro

BG: background augmented, training fatto su immagini prese dal cleaned con sfondi aumentati

C+BG: entrambi

## REPORTS (e test)

report_(modello A o B)_(Test)

### Test

Test1: su modello C, testet cleaned

Test2: su modello C, testet realistico

(!!!Attenzione a prendere lo split corretto, il modello non deve aver mai visto le immagini di test!!!)

Test3: su modello C, testset cleaned con background aumentato

Test4: su modello BG, testset cleaned

Test5: su modello BG, testset realistico

Test6: su modello BG+C, testset cleaned

Test7: su modello BG+C, testset realistico

