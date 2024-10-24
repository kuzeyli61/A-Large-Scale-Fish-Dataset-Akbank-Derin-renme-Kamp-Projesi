# A-Large-Scale-Fish-Dataset-Akbank-Derin-renme-Kamp-Projesi

# Projenin Amacı

Resimi inceleyerek balığın hangi tür balık olduğunu tespit eden ANN algoritması geliştirmek.

# Proje Detayları

Projemde biri pretrained diğeri cnn olan iki projeden esinlendim. Çünkü ilk defa Deep Learning projesi yaptım. Ancak hiçbir şekilde pretrained ve CNN modeli kullanmadım. Model tamamen bana aittir. Veri setinin keşifçi analizi ve değerlendirmesini ise özgünleştirdim.

# Proje Adımları

Modeli ilk başta 64 layerdan oluşan tek bir hidden layer ile başladım ve "Test Accuracy" değerim %70 olarak çıktı.
Daha sonra aşağıdaki belirteceğim şekilde modeli güncelledim

Deneme 2 :
  64 nöronluk 2 hidden layer eklendi
  Test Accuracy : % 80

Deneme 3:
  batch_size = 32' den 64'e çıkartıldı
  Test Accuracy: %89

Deneme 4:
  epochs = 10'dan 20'ye çıkartıldı
  Test Accuracy: %88

Deneme 5:
  3. hidden layer eklendi
  17. epoch'ta model durdu
  Test Accuracy: %92

Deneme 6:
  Overfitting'ten kaçınmak için "Dropout = 0.3" eklendi
  10. epoch'ta model durdu
  Test Accuracy: %86

Deneme 7:
  Nöron sayıları 128'e çıkartıldı
  Test Accuracy: %88

Deneme 8:
  4. hidden layer eklendi
  Test Accuracy: %86

Deneme 9:
  batch_size = 128 olarak güncellendi
  Hidden layer sayısı 3'e indirildi
  Test Accuracy: %90

Deneme 10:
  Learning rate parametresi 0.001 olarak eklendi
  Test Accuracy: %91

Deneme 11:
  Dropout = 0.01 olarak güncellendi
  Test Accuracy: %91

Deneme 12:
  Learning rate parametresi 0.01 olarak güncellendi
  Test Accuracy: %83

Deneme 13:
  Learning rate parametresi 0.005 olarak güncellendi
  Test Accuracy: %84

Deneme 14:
  Learning rate parametresi 0.001 ' e geri getirildi ve en doğru değer olarak karar kılındı.
  Test Accuracy: %95

14. denemede modelin en doğru hiperparametre optimizasyonu olduğuna karar kıldım. Her bir denemede Confussion Matrix'i inceledim ve overfitting ya da underfitting olup olmadığına karar verdim. Diogonal çizgideki değerler 90+ iken kalan değerler 0.01'in altındaydı.
Eğer değerler karmaşık olsaydı underfittin, diogonal çizgideki değerler dışındaki sonuçlar da yüksek olsaydı overfitting olduğunu düşünürdüm. Bu sayede Confussion Matrix'in önemini çok iyi kavradım.

Modelimdeki Diğer Hiperparametreler

Adam : Gelişmiş Gradydan Alçalış metodu olduğu için tercih ettim.
categorical_crossentropy : Okuduğum makalelerde ve incelediğim projelerde bunun en uygun fonksiyon olduğunu öğrendim.
relu: Pikselleri 0-1 aralığına indirgediğim için matematiksel formülünden dolayı bunu kullanmayı tercih ettim.
softmax: Okuduğum makalelerde ve incelediğim projelerde bunun en uygun fonksiyon olduğunu öğrendim.

kaggle: https://www.kaggle.com/code/embiyasarca/fish-ann-projects

Dipnot: Nedenini anlamadığım bir şekilde Kaggle'da projemi save & push ederken kodumda hatalar olduğunu gösteriyordu bu yüzden tekrar tekrar yüklemeyi denemek zorunda kaldım. Formu zamanında doldurdum, projemde ise majör bir değişiklik yapmadım.


























