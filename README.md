# Tutorial 9 Adpro 
**Emanuella Abygail - 2306152185**

## What is amqp?
AMQP (Advanced Message Queuing Protocol) adalah protokol komunikasi jaringan terbuka yang dirancang untuk mengirimkan pesan antar aplikasi, komponen, atau sistem yang berbeda secara asinkron. Protokol ini digunakan dalam message-oriented middleware yang memungkinkan berbagai jenis komunikasi seperti message queuing, publish-subscribe, dan request-response. AMQP mendefinisikan message structure, exchange rules, dan operasi-operasi yang dapat dilakukan pada pesan.

Pada tutorial ini, AMQP digunakan untuk membuat sistem message queue yang memungkinkan aplikasi menerima dan memproses pesan secara asinkron. Penggunaan AMQP terlihat pada pendefinisian pesan pada `UserCreatedEventMessage`, pembuatan handler untuk menerima pesan (`impl MessageHandler<UserCreatedEventMessage> for UserCreatedHandler`), inisialisasi listener AMQP pada `let listener`, menunggu pesan pada `_ = listener.listen(...)`, dan infinite looping (`loop {}`)

## What does it mean? guest:guest@localhost:5672 , what is the first guest, and what is the second guest, and what is localhost:5672 is for?
`guest` pertama pada `guest:guest` adalah username, sedangkan yang kedua adalah password. `localhost` adalah alamat host dari AMQP broker (server RabbitMQ). `:5672` adalah port di mana AMQP broker sedang listening. `guest:guest@localhost:5672` secara keseluruhan adalah URL yang menyambungkan ke server AMQP.