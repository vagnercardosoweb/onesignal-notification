## PushNotification [ONESIGNAL](https://onesignal.com/)

Para utilização da classe é só seguir os passos abaixo.

- **appId:** Chave do aplicativo criado.
- **appKey:** Chave para a autenticação.

````php
<?php
  // Instancia a classe
  $push = new PushNotification('appId', 'appKey');

  // Envia notificação
  $params = array(
      'included_segments' => array('All'),
      'url' => 'https://navegarte.com/',
      'ios_attachments' => array("id" => 'https://cdn.pixabay.com/photo/2016/04/15/04/02/water-1330252_960_720.jpg'),
      'headings' => array("en" => 'Testando pela class'),
      'contents' => array("en" => 'Resposta pela class'),
      'ios_badgeType' => 'Increase',
      'ios_badgeCount' => 1,
      'big_picture' => 'https://cdn.pixabay.com/photo/2016/04/15/04/02/water-1330252_960_720.jpg',
      'isIos' => true,
      'isAndroid' => true,
      'android_sound' => 'default',
      'ios_sound' => 'default'
  );

  var_dump($push->sendNotification($params));

  // Lista todas notificação
  //var_dump($push->allNotifications(200, 0));

  // Vizualiza determinada notificação
  //var_dump($push->viewNotification('notificationId'));
````
