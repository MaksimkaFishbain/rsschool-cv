![resume](https://user-images.githubusercontent.com/95378394/207242388-ea7e2605-cb7a-4a8e-bdcd-88b2ca27933f.png)

<h1>name: Maxim Fishbine</h1>

<ol> contacts:
<li> tg: @magsador;
<li> vk: vk.com/donformatik;
<li> mail: maksim_fb@mail.ru;
<li> gmail: bbadboy1337@gmail.com;
<li> Rc-School: @donformatik;
</ol>

<ul> aboutMe: <li> At the moment my goal is to master front-end development, in the future I think to become a full-stack developer, good luck to me);</li>
<li> My strengths: diligence, discipline, patience, enthusiasm; </li>
<li> I didn’t have any work experience yet, I did independent projects, I’m happy to receive new knowledge in order to improve my skills.</li>
<li> <ul>
<li>Delphi (low level)</li>
<li>C# (low level)</li>
<li>Golang (low level)</li>
<li>Python and Django framework (middle)</li>
<li>html сss (middle)</li>
<li>JS (middle)</li>
<li>React (low)</li>
</ul>
</li>
</ul>

<h3>3.5 My code Django (create model card pizza for sqlite):</h3>

```
from django.db import models
from django.urls import reverse
class Card(models.Model):
title = models.CharField(max_length=25, verbose_name='Название')
image = models.ImageField(upload_to="pizzaImage/", verbose_name='Картинка')
price = models.PositiveIntegerField(verbose_name='Цена')
modalContent = models.TextField(blank="True", verbose_name='Описание')
isMeat = models.PositiveIntegerField(verbose_name='Тип пиццы(0/1)')
popularity = models.PositiveIntegerField(verbose_name='Популярность')
date_create = models.CharField(max_length=10, verbose_name='Дата создания')
date_update = models.CharField(max_length=10, verbose_name='Дата обновления')

def __str__(self):
return self.title

def get_absolute_url(self):
return reverse('Card', kwargs={'название': self.title})

class Meta:
verbose_name='Карточки пицц'
verbose_name_plural='Карточки пицц'
ordering=['date_create','title']
```

<h3>Transferring data to json format for working with them in js:<h3>

```
from card.models import Card
from django.core import serializers
from django.http import JsonResponse
import json

with open('frontend/src/infoCard.json','w',encoding='utf-8') as file:
json.dump([*Card.objects.values()],file,indent = 2,ensure_ascii=False)
```

<h3>My code react (create cart for shop):</h3>

```
const Cart = ({cartOpened, setCartOpened, cartContent, setCartContent, cost}) => {
console.log('cartContent', cartContent)
return (
<div className={cartOpened ? "cart" : "cart.active"} onClick={() => setCartOpened(false)}>
<div className={cartOpened ? "cart__content" : "cart.active"} onClick={e => e.stopPropagation()}>
<div className="cartHeader">
<h1>Корзина</h1>
<img src={"/media/сancel.png"} alt={"close cart"} onClick={() => setCartOpened(false)}/>
</div>
<div className="cartItems">
{cartContent.map((cartItem, index) =>
<CartItem
key={index}
cartContent={cartContent}
setCartContent={setCartContent}
{...cartItem}
/>
)}
</div>
<div className="orderButton">
<p>Оформить заказ на <marker>{cost}</marker> руб.</p>
</div>
</div>
</div>
);
};
```

<h3>my code JS(audio player):</h3>

```
const audio1 = document.querySelector('.audio1'),
audio2 = document.querySelector('.audio2'),
nameSong1 = document.querySelector('.nameSong1'),
nameSong2 = document.querySelector('.nameSong2'),
albumImage = document.getElementById('album'),
playStop1 = document.getElementById('1'),
playStop2 = document.getElementById('2'),
avatar = document.querySelector('.avatarInst'),
link = document.querySelector('.link')

let stop = true

function loadSong(nameSong,playStop,audio) {
stop = false
audio.play()
nameSong.classList.add('play')
albumImage.classList.add('active')
playStop.textContent = '❚❚'

}

function stopSong(nameSong,playStop,audio) {
stop = true
audio.pause()
nameSong.classList.remove('play')
albumImage.classList.remove('active')
playStop.textContent = 'ᐅ'

}

nameSong1.addEventListener('click', () =>{

stop===true?loadSong(nameSong1,playStop1,audio1):stopSong(nameSong1,playStop1,audio1)
})

nameSong2.addEventListener('click',
() =>{

stop===true?loadSong(nameSong2,playStop2,audio2):stopSong(nameSong2,playStop2,audio2)
})
```

<h3> Doing a project with a friend - https://github.com/MaksimkaFishbain/dj_react_pizza.git </h3>

<h3> I study to be a software engineer in college, I went to a course on the basics of js by our teacher. </h3>

<h3> I rate myself at level A1.</h3>
