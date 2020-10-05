# my-django-doc
Django projelerime başlarken işimi kolaylaştırmak adına oluşturduğum bir repositorydir.

Repository'de bulunanlar:

Django Rest Framework (api servisi için)
django-hosts (özel subdomain yönlendirmeleri için)



İsteğe bağlı virtualenv paket kurulumu: 

```powershell
pip install virtualenv
```

Daha sonrasında gereken paketleri kuruyoruz. Gereken paketleri görmek için requirements.txt dosyasını inceleyebilirsiniz

```powershell
pip install -r requirements.txt
```


Account custom user modelinin ve veritabanının oluşturulması için alttaki komutları sırasıyla çalıştırın.
```powershell
cd devstone
python manage.py makemigrations
python manage.py migrate
```


## Klasörler

### api 

Bu klasör api subdomaininin yönlendirmeleri ve kodlarını yazmak içindir.

**urls.py** dosyasının içerisine: 
```python
path('helloworld/', views.index ,name='index')
```
şeklinde path ekleyebilirsiniz. Host Domainimizin localhost:8000 olduğunu düşünürsek eğer `api.localhost:8000/helloworld` şeklinde yazdığınız url çağrılabilir. 

### account 

Bu klasör içerisinde kendi yarattığım custom user model bulunmaktadır.