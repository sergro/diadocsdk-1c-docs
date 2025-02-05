﻿CreateSendTaskFromFile
======================

Метод объекта :doc:`Organization <Organization>`

**Синтаксис**


CreateSendTaskFromFile(<Path>, <Type>)

**Параметры**


-  <Path> (строка, обязательный) - путь до файла
-  <Type> (строка, обязательный) - тип отправляемого документа

Параметр Type может принимать одно из следующих значений:

-  "InvoiceContent" - отправка счета-фактуры, исправления счета-фактуры
-  "InvoiceCorrectionContent" - отправка корректировочного
   счета-фактуры, исправления корректировочного счета-фактуры
-  "XmlAcceptanceCertificateContent" - отправка формализованного акта о
   выполнении работ в формате xml
-  "XmlTorg12Content" - отправка формализованной ТОРГ-12 в формате xml
-  "UniversalTransferDocument" - отправка универсального передаточного документа
-  "NonformilizedDocumentContent" - отправка произвольного
   неформализованного документа
-  "AcceptanceCertificateContent" - отправка неформализованного акта о
   выполнении работ
-  "Torg12Content" - отправка неформализованной ТОРГ-12
-  "ProformaInvoiceContent" - отправка неформализованного счета на
   оплату
-  "XmlContent" - отправка произвольного формализованного документа в
   формате xml
-  "Contract" - отправка договора
-  "CertificateRegistry" - отправка реестра сертификатов
-  "PriceListAgreement" - отправка протокола согласования цены
-  "ReconciliationAct" - отправка акта сверки
-  "ServiceDetails" - отправка детализации
-  "UtdTorg12" - отправка формализованной ТОРГ-12 в формате УПД
-  "UtdAcceptanceCertificate" -  отправка формализованного акта о
   выполнении работ в формате УПД
-  "UtdInvoice" -  отправка счета-фактуры в формате УПД
-  "UcdInvoiceCorrection" - корректировка счета-фактуры в формате УКД

**Возвращаемое значение**


Объект :doc:`SendTask <SendTask>`.

**Описание**


Позволяет создать задание для отправки документа на сервер Диадок на
основе сформированного файла.
