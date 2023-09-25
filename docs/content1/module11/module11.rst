SSL復号バイパスルールの設定（クライアントIPサブネット）
=========================================================

SSLOでは、SSL復号をバイパスするためのルールを柔軟に設定可能です。ここでは、特定のクライアントIPサブネットからのアクセスは、SSL復号をバイパスする設定を行います。

#. **SSL Orchestrator >> Configuration** にて、**Security Policies** を選択します。

   .. image:: images/mod11-1.png
   |  
#. 作成済みのポリシーを選択します。

   .. image:: images/mod11-2.png
   | 
#. 前項で作成したバイパスルールを一旦削除します。

   .. image:: images/mod11-3.png
   | 
#. :guilabel:`OK` ボタンを押します。

    .. image:: images/mod11-4.png
    |  
#. :guilabel:`Add` を押します。

   .. image:: images/mod11-5.png
   | 
#. **Name** に任意の名前を設定し、**Conditions** にて **Client IP Subnet Match** を選択し、バイパスさせたいサブネットを設定し（F5ハンズオンでは、10.1.10.0/24）、**SSL Forward Proxy Action** にて **Bypass** を選択し、SSL復号していないトラフィックもセキュリティデバイスに転送したい場合は、**Service Chain** も選択し、:guilabel:`OK` を押します。

   .. image:: images/mod11-6.png
   | 
#. バイパスルールが設定されていることを確認し、:guilabel:`Deploy` を押します。

   .. image:: images/mod11-7.png
   |  
#. 編集の確認が表示されるので、:guilabel:`OK` ボタンを押します。

    .. image:: images/mod11-8.png
    | 
#. Successポップアップが表示されます。:guilabel:`OK` ボタンを押します。

    .. image:: images/mod11-9.png
    |  

.. note::
    - URL Filteringカテゴリ、宛先のIPサブネット、ポート番号、プロトコルタイプ、URL、IPジオロケーションなどでもSSL復号パイパスの設定が可能です。
    - セキュリティデバイスがICAPサービス、HTTPサービスの場合、SSL復号していないトラフィックをサービスチェーンに流せません。

