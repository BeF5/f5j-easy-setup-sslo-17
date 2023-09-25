SSL復号バイパスルールの設定（URL Filteringカテゴリ）
=========================================================

SSLOでは、SSL復号をバイパスするためのルールを柔軟に設定可能です。ここでは、特定カテゴリのサイト（例：金融、ヘルスケア）へのアクセスは、SSL復号をバイパスする設定を行います。

.. note::
    管理者が設定した接続先でルールを設定することもできますが、一般的なカテゴリルールを利用したい場合、別途URL Filteringのサブスクリプションライセンスが必要となります。また、URL Filteringのプロビジョニング、URL Filtering DBのダウンロードが必要です。（F5ハンズオンでは予め、URL Filtering DBを設定、ダウンロードしてあります。）

#. **SSL Orchestrator >> Configuration** にて、**Security Policies** を選択します。

   .. image:: images/mod9-1.png
   |  
#. 作成済みのポリシーを選択します。

   .. image:: images/mod9-2.png
   | 
#. :guilabel:`Add` を押します。

   .. image:: images/mod9-3.png
   | 
#. **Name** に任意の名前を設定し、**Conditions** にて **Category Lookup(All)** を選択し、バイパスさせたいカテゴリを選択し、**SSL Forward Proxy Action** にて **Bypass** を選択し、SSL復号していないトラフィックもセキュリティデバイスに転送したい場合は、**Service Chain** も選択し、:guilabel:`OK` を押します。

   .. image:: images/mod9-4.png
   | 
#. バイパスルールが設定されていることを確認し、:guilabel:`Deploy` を押します。

   .. image:: images/mod9-5.png
   |  
#. ポップアップが表示された場合、:guilabel:`Deploy` を押します。

   .. image:: images/mod9-7.png
   |  
#. Successポップアップが表示されます。:guilabel:`OK` ボタンを押します。

    .. image:: images/mod9-6.png
    |  

.. note::
    - 送信元、宛先のIPサブネット、ポート番号、プロトコルタイプ、URL、IPジオロケーションなどでもSSL復号パイパスの設定が可能です。
    - セキュリティデバイスがICAPサービス、HTTPサービスの場合、SSL復号していないトラフィックをサービスチェーンに流せません。

