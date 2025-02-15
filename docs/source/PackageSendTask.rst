﻿PackageSendTask
===============

Объект предназначен для отправки сообщения с пакетом документов на сервер Диадок.

Свойства
--------

-  **Content** (чтение/запись) - содержание пакета документов, имеет тип 
   :doc:`SentPackageContent <SentPackageContent>`
-  **OperationId** (строка, чтение/запись) - уникальный идентификатор
   операции. Если отправка пакета с заполненным оператором операции завершилась успехам, то все остальные попытки отправки с тем же идентификатором не будут приводить к отправке нового пакета, а в результате выполнения метода вернется ссылка на ранее отправленный пакет.
-  **CounterAgentId** (строка, чтение/запись) - идентификатор контрагента
-  **FromDepartmentId** (строка, чтение/запись) - идентификатор
   подразделения отправителя
-  **ToDepartmentId** (строка, чтение/запись) - идентификатор подразделения
   получателя
-  **IsDraft** (булево, чтение/запись) - признак того, что сообщение является
   черновиком
-  **IsInternal** (булево, чтение/запись) - признак того, что сообщение
   является внутренним, то есть сообщением между подразделениями
   организации
-  **LockPackage** (булево, чтение/запись) - признак того, что пакет после
   отправки должен быть нередактируемым
-  **DelaySend** (булево, чтение/запись) - признак того, что сообщение будет
   сохранено без отправки
-  **DocumentsToSend** (:doc:`коллекция <Collection>` объектов :doc:`DocumentToSend <DocumentToSend>`, чтение) -
   коллекция документов, уже добавленных в пакет
-  **ProxyBoxId** (строка, чтение/запись) - идентификатор ящика, промежуточного получателя. Если указан ящик промежуточного получателя, то документа доставится конечному получателя только после того, как промежуточный получатель поставит подпись под документом. Если промежуточный получатель            отклонит документ, то в ящик конечного получателя он не будет доставлен
-  **ProxyDepartmentId** (строка, чтение/запись) -  идентификатор подразделения, в ящике промежуточного получателя
-  **UseShelf** (булево, чтение/запись) - использовать отправку "с полки" (для больших документов)

Методы
------

-  :doc:`AddDocument <AddDocument>` - добавляет документ заданного типа
   в пакет на отправку
-  :doc:`AddDocumentFromFile <AddDocumentFromFile>` - добавляет документ 
   в пакет на отправку, загружая его из файла
-  :doc:`AddDocumentFromFileRaw <AddDocumentFromFileRaw>` - добавляет документ 
   в пакет на отправку, загружая его из файла (без парсинга) 
-  :doc:`Send <Send-(PackageSendTask)>` - отправляет пакет документов на сервер
-  :doc:`SendAsync <SendAsync-(PackageSendTask)>` - инициирует асинхронную отправку 
   пакета документов
-  :doc:`AddEncryptCertificate <AddEncryptCertificate-(PackageSendTask)>` - добавляет сертификат шифрования документа

.. toctree::
   :name: Auto
   :hidden:

   AddDocument <AddDocument>
   AddDocumentFromFile <AddDocumentFromFile>
   AddDocumentFromFileRaw <AddDocumentFromFileRaw>
   Send <Send-(PackageSendTask)>
   SendAsync <SendAsync-(PackageSendTask)>
   AddEncryptCertificate <AddEncryptCertificate-(PackageSendTask)>