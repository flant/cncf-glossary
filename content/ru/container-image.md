---
title: Образ контейнера
status: Feedback Appreciated
category: concept
tags: ["", "", ""]
---

## Описание

Образ контейнера — это неизменяемый статический файл, содержащий зависимости, необходимые для создания [контейнера](/container/).
Эти зависимости могут включать один исполняемый двоичный файл, 
системные библиотеки, системные инструменты, переменные окружения и другие необходимые настройки платформы.
Образы контейнеров являются результатом [контейнеризации](/containerization/) приложения и обычно хранятся в реестрах контейнеров, 
откуда их можно скачать и запустить как изолированный процесс с помощью интерфейса исполнения для контейнеров (Container Runtime Interface, CRI).
Фреймворк, с помощью которого создается образ контейнера, должен соответствовать стандартной схеме, определенной инициативой Open Container Initiative (OCI).

## Проблема

Традиционно серверы настраиваются под каждое окружение, и на них развертываются приложения.
Любое несоответствие конфигурации окружений — большая проблема, которая часто приводит к простоям или неудачным развертываниям.
Окружение приложения должно быть повторяемым и строго определенным; 
в противном случае возрастает вероятность возникновения ошибок, связанных с окружением.
Если окружение настроено неадекватно или с ошибками, [горизонтальное](/horizontal-scaling/) и [вертикальное](/vertical-scaling/) масштабирование приложений становится проблематичным.

## Решение

Образы контейнеров содержат приложение с любыми его рантайм-зависимостями, например, с сервером этого приложения.
Это позволяет добиться согласованности во всех окружениях, включая компьютер разработчика.
Образы контейнеров могут использоваться для запуска необходимого количества контейнеров, что облегчает [масштабирование](/scalability/).