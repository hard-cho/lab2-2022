# Разработка игры Dragon Picker
Отчет по лабораторной работе #2 выполнила:
- Россихина Ирина Александровна
- РИ-300002

Отметка о выполнении заданий (заполняется студентом):

| Задание | Выполнение | Баллы |
| ------ | ------ | ------ |
| Задание 1 | * | 60 |
| Задание 2 | # | 20 |
| Задание 3 | # | 20 |

знак "*" - задание выполнено; знак "#" - задание не выполнено;

Работу проверили:
- к.т.н., доцент Денисов Д.В.
- к.э.н., доцент Панов М.А.
- ст. преп., Фадеев В.О.

[![N|Solid](https://cldup.com/dTxpPi9lDf.thumb.png)](https://nodesource.com/products/nsolid)

[![Build Status](https://travis-ci.org/joemccann/dillinger.svg?branch=master)](https://travis-ci.org/joemccann/dillinger)

Структура отчета

- Данные о работе: название работы, фио, группа, выполненные задания.
- Цель работы.
- Задание 1.
- Выводы.

## Цель работы
Начать разработку игры Dragon Picker.

## Задание 1
### Пошагово выполнить каждый пункт раздела "ход работы" с описанием и примерами реализации задач по теме видео самостоятельной работы.
Ход работы:
В этой части создаём дракона, учим его летать и сбрасывать яйца. Добавляем визуальные эффекты для столкновения яйца с землёй.
1) Создать новый проект.

![создаём проект](https://user-images.githubusercontent.com/74662720/195043407-02f0181a-f00a-4611-b10c-3d72048e1583.png)

3) Загрузить пакет Dragon for Boss Monster из Unity Asset Store.

![нашли ассет](https://user-images.githubusercontent.com/74662720/195043465-19452e0a-3eba-4b10-b1b4-e9d889e41586.png)

Загрузить и импортировать пакет в Unity

![загружен, сейчас будем импортировать](https://user-images.githubusercontent.com/74662720/195043766-c6d6fd8b-c4c4-434c-a6ab-912c477a0e7d.png)


5) Выбрать понравившегося дракона, создать его дубликат.

![создали дубликат понравившегося дракона](https://user-images.githubusercontent.com/74662720/195043979-60ab8029-0560-4bc3-8177-b89cef79bfa7.png)

Дубликат в свою очередь переместить в папку Scenes.

![перетащили](https://user-images.githubusercontent.com/74662720/195044029-5811c4f8-0aed-4219-af4c-5aca5dde7b61.png)

8) Дать дубликату имя Enemy и переместить в иерархию. Настроить координаты Position и Rotation на значения: 0; 0; 0.

![переименовали и перетащили в окно иерархии](https://user-images.githubusercontent.com/74662720/195044314-b5eb3713-b95d-4ded-ac90-20406053e89d.png)

10) Создать Animation Controller с названием EnemyCTRL.

![вот так выглядит окно с конролем анимации](https://user-images.githubusercontent.com/74662720/195077144-6ff05191-a05f-440f-a05b-dc0b9028e405.png)

12) В папке Animations найти анимацию полёта, создать её дубликат. Дубликат перетащить в окно анимации EnemyCTRL.

![в окне анимации](https://user-images.githubusercontent.com/74662720/195078636-103d9419-f2bf-471e-b2fb-502bcb550e61.png)

13) Подключить EnemyCTRL к объекту Enemy.

![подключили анимацию](https://user-images.githubusercontent.com/74662720/195078742-eff93f4f-daa5-42d6-87b2-b2c71c2cfc89.png)

17) Создать сферу Egg, которая будет драконьим яйцом. Настроить параметр Scale на значения: 1; 1.5; 1.

![создали яйцо](https://user-images.githubusercontent.com/74662720/195044889-67a9b3ff-8aad-40bb-8066-b75a1e90fc86.png)

16) Создать материал Mat_Egg, настроить его. Добавить материал к объекту Egg.

![применили материал на яйцо](https://user-images.githubusercontent.com/74662720/195045493-c852b9ef-5cdb-4227-bcd8-c32b1e9517ff.png)

18) Добавить к Egg компонент RigidBody.

![добавили rigidbody](https://user-images.githubusercontent.com/74662720/195045557-35b9d59c-55c8-4e78-8376-c528e5e77bcb.png)

20) Создать тег Dragon Egg и добавить его к объекту Egg.

![поменяли тэг](https://user-images.githubusercontent.com/74662720/195045755-1cb4c48b-8de6-46b7-b4cf-8a18e6f4f38c.png)

22) Сделать из Egg префаб и удалить объект со сцены.

![создали префаб](https://user-images.githubusercontent.com/74662720/195046000-d706fca3-2662-4507-86f5-509c5598107b.png)

24) Создать сферу Shield. Настроить параметр Scale на значения: 3; 3; 3.

![создали эн щит](https://user-images.githubusercontent.com/74662720/195076429-de5c2f5e-59ae-4a6a-971b-447c8f10d9c2.png)

26) Создать материал для щита и назначить ему свойство Transparent в поле Rendering Mode. Добавить материал к щиту.

![настроили материал и применили на энщит](https://user-images.githubusercontent.com/74662720/195076770-2ee18d22-702a-43ae-8910-7fbfb2cefe74.png)

28) Добавить к Shield компонент RigidBody. Отключаем гравитацию и включаем кинематику.

![на эн щит добавим rigidbody](https://user-images.githubusercontent.com/74662720/195076852-75ef1648-5cb1-414f-a004-2b98dba88fdd.png)

30) Сделать из Shield префаб

![создали префаб из щита](https://user-images.githubusercontent.com/74662720/195076913-56ca0ea2-16e5-4567-a8ef-f5ecbfe9a826.png)

32) Настроить камеру и игровую область.

![настроили камеру и игровую область](https://user-images.githubusercontent.com/74662720/195079034-b6997a67-0b89-490d-b0d3-80e4a14b0264.png)

34) Написать скрипт EnemyDragon для передвижения дракона и подключить его к Enemy.

        using System.Collections;
        using System.Collections.Generic;
        using UnityEngine;

        public class EnemyDragon : MonoBehaviour
        {
            public GameObject dragonEggPrefab;
            public float speed = 1f;
            public float timeBetweenEggDrops = 1f;
            public float leftRightDistance = 10f;
            public float chanceDirection = 0.1f;

            // Start is called before the first frame update
            void Start()
            {
                
            }

            // Update is called once per frame
            void Update()
            {
                Vector3 pos = transform.position;
                pos.x += speed * Time.deltaTime;
                transform.position = pos;

                if (pos.x < -leftRightDistance)
                {
                    speed = Mathf.Abs(speed);
                }

                if (pos.x > leftRightDistance)
                {
                    speed = -Mathf.Abs(speed);
                }
            }

            private void FixedUpdate()
            {
                if (Random.value < chanceDirection)
                {
                    speed *= -1;
                }
            }
        }

36) Установить значения в окне Inspector.

![прикрепили скрипт и поменяли значения](https://user-images.githubusercontent.com/74662720/195079134-6105a2df-c0dc-4bea-9029-17754faa0e64.png)

37) В поле Dragon Egg Prefab вложить префаб яйца.

![добавили префаб яйца](https://user-images.githubusercontent.com/74662720/195080334-c619dc89-988a-4a1c-afb7-cb3ea2bb6228.png)

39) Изменить скрипт. Добавить код в метод Start и создать новый метод DropEgg

            void Start()
            {
                Invoke("DropEgg", 2f);
            }

            void DropEgg()
            {
                Vector3 myVector = new Vector3(0.0f, 5.0f, 0.0f);
                GameObject egg = Instantiate<GameObject>(dragonEggPrefab);
                egg.transform.position = transform.position + myVector;
                Invoke("DropEgg", timeBetweenEggDrops);
            }
41) По аналогии с пакетом Dragon for Boss Monster добавить и импортировать пакет Fire & Spell Effects из Unity Asset Store.

![нашли ассет](https://user-images.githubusercontent.com/74662720/195080788-f1ef769f-087f-4f77-8883-9164c6fce903.png)

43) Добавить плоскость Ground и настроить её.

![добавили Plane и изменили параметры](https://user-images.githubusercontent.com/74662720/195084517-21da50b5-f76f-4d9a-9b35-56b5397fe48d.png)

45) Добавить материал к плоскости.

![добавили материал для plane](https://user-images.githubusercontent.com/74662720/195084646-3dc63f28-278b-4a42-bf66-a5aa509f3247.png)

47) Создать скрипт DragonEgg и подключить его к Egg.

        using System.Collections;
        using System.Collections.Generic;
        using UnityEngine;

        public class DragonEgg : MonoBehaviour
        {
            public static float bottomY = -30f;
            // Start is called before the first frame update
            void Start()
            {

            }

            private void OnTriggerEnter(Collider other)
            {
                ParticleSystem ps = GetComponent<ParticleSystem>();
                var em = ps.emission;
                em.enabled = true;

                Renderer rend;
                rend = GetComponent<Renderer>();
                rend.enabled = false;
            }

            // Update is called once per frame
            void Update()
            {
                if (transform.position.y < bottomY)
                {
                    Destroy(this.gameObject);
                }
            }
        }

49) Добавить к яйцу компонент Particle System. Настроить этот компонент.

![настройка particle system 1](https://user-images.githubusercontent.com/74662720/195085474-edad5452-09f9-4ba1-88a8-6bbb16725409.png)

![настройка particle system 2](https://user-images.githubusercontent.com/74662720/195085490-9f33f7c7-8b42-462d-9030-94f255850a83.png)

51) В компоненте Mesh Collider включить свойство IsTrigger у объекта Ground.

![добавили триггер для плоскости](https://user-images.githubusercontent.com/74662720/195085664-2ef534d1-b97e-48c3-9b31-27d1dd8c64ba.png)

53) Создать скрипт DragonPicker и подключить его к камере.

        using System.Collections;
        using System.Collections.Generic;
        using UnityEngine;

        public class DragonPicker : MonoBehaviour
        {
            public GameObject energyShieldPrefab;
            public int numEnergyShield = 3;
            public float energyShieldBottomY = -6f;
            public float energyShieldRadius = 1.5f;

            void Start()
            {
                for (int i = 1; i <= numEnergyShield; i++)
                {
                    GameObject tShieldGo = Instantiate<GameObject>(energyShieldPrefab);
                    tShieldGo.transform.position = new Vector3(0, energyShieldBottomY, 0);
                    tShieldGo.transform.localScale = new Vector3(1*i, 1*i, 1*i);
                }
            }

            void Update()
            {

            }
        }

55) В Energy Sheild Prefab добавить префаб щита.

![Добавили скрипт и префаб в скрипт](https://user-images.githubusercontent.com/74662720/195087265-eab7b84d-abe6-418e-bf9e-3cdf4fe65a93.png)

57) Удалить щит.
58) Проверить, что всё получилось.

https://user-images.githubusercontent.com/74662720/195087702-c046723c-66cb-4b85-80ff-1a8f0382f903.mp4


## Заполняем поля в консоли разработчика в Яндекс.Играх.
![поле 1](https://user-images.githubusercontent.com/74662720/195088213-694129d7-a455-4bb5-b51f-d2bf78b17658.png)
![поле 2](https://user-images.githubusercontent.com/74662720/195088203-0d5be026-c403-413e-b0e2-c1f6f9068910.png)
![поле 3](https://user-images.githubusercontent.com/74662720/195088208-22556906-4b70-48b7-9c63-89094e59e859.png)

## Выводы

В ходе лабораторной работы была начата разработка игры Dragon Picker. Был создан дракона, который умеет летать и сбрасывать яйца. Были добавлены визуальные эффекты. Также были заполнены некоторые поля в черновике на Яндекс.Играх. В будущем продолжится заполнение черновика.


## Powered by

**BigDigital Team: Denisov | Fadeev | Panov**
