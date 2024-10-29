# Aygaz-Machine-Learning-Project
Aygaz Makine Öğrenmesi Bootcampinde yaptığım projedir. Supervised ve unsupervised öğrenme tiplerini karşılaştırdım.

Aygaz Makine Öğrenmesi Bootcampinde yapmaya çalıştığım projedir. Supervised ve unsupervised öğrenme tiplerini karşılaştırdım.

Öncelikle projenin kaggle linki : https://www.kaggle.com/code/nezirerdinc/aygaz-ml-bootcamp

Projeyi yaparken " US Accidents (2016 - 2023) " veri setini kullandım. Veri Seti linki : https://www.kaggle.com/datasets/sobhanmoosavi/us-accidents

## Projede kullandığım kütüphaneler

Numpy, pandas, matplotlid, seaborn, warnings, sklearn,

# Eda ve Veri Düzenleme

Öncelikle veri setinin keşfini yaptım, bu keşiften yola çıkarak işime yarayabilecek etiketlere baktım.Ondan sonra kullanabileceğim etiketler üzerinde iyileştirme yaptım ve ml parametresi olarak kullanaiblmek için kaza toparlama süresini parçalar ayırdım.

## One-Hot Encoding ve Unsupervied,Supervised Ml

Bütün veri ile çalışamayacağımdan dolayı veriyi ilk olarak bölgeler ve sonra ilçelere kadar küçültüyorum.Küçültmeden sonra verileri sayısal veriye dönüştürmek için one-hot encoding yapıyorum. Gelen dummiese target ve kullanacağı parametereleri öğretiyorum ve eğitim ve test datasını ayırıyorm.Random state=42 seçip test_size=0.3 üzerinde çalışıyorum.

Supervised olarak ilk lojistik regresyon üzerinde çalışıyorum California|Los angeles ilçesi için lojistik regresyondan accuracy_score 0.813 buluyorum. Supervised olarak ikinci olarak Knn çalışıtırıyorum (en yakın komşu algoritması) knn için 6 yakınlık kullandım. Knn'in scorunu 0.848 olarak buluyorum burada knn daha tutarlı çalışıyor gibi. Sizin verdiğiniz eğitimdeki sınıflandırma raporu ve karmaşıklık matrisini de knn üzerinde uyguladım.

Unsupervised olarak sadece K-means olarak kullandım. Baktığım dökümantasyonda scaler kullanıyordu ama benim datam zaten one-hot encoding yapıldığı için kullanmadım ama emin de olamadım.Hocamızın derste kullandığı k-elbowu bulmak için bir kod parçacığından yararlandım. Dirseği 4-6 gibi buldum.K-means'ı 6 cluster ve random_state'i 42 olarak seçip eğittim.Adjusted rand indexi. 1'in altında bir rakam buldum.Bu çok başarılı bir sonuç değil.

Yani sonuç olarak benim seçtiğim şehir ve ilçeye göre Supervised'ın knn algoritması en başarılı olarak çalıştı.

Projemi incelediğiniz için teşekkür ederim.
