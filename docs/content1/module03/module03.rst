ライセンスアクティベーション、プロビジョニング、CA証明書／鍵登録
=========================================================

（ **※F5ハンズオンでは以下設定済みです。** ） 

#. :guilabel:`Next` ボタンを押します。
   
   .. image:: images/mod3-1.png
   |  
#. ライセンスをアクティベーションします。
   
   |  
#. 以下のモジュール（SSL復号／再暗号化： **SSLO** )をプロビジョニングします。（F5ハンズオンでは、1.9章で利用するURL Filteringのカテゴリ利用のために、**URLDB** 、現在手順にはありませんがプロキシ認証を行うための **APM** もプロビジョニングしています。ライセンスはSSLOとAPMの２つと、URL Filteringサブスクリプションを利用しています。）
    
   .. image:: images/mod3-2.png
   |  
#. :guilabel:`Next` ボタンを押します。
   
   .. image:: images/mod3-3.png
   |  
#. **ホスト名**、**タイムゾーン**、**Rootパスワード** を設定して、:guilabel:`Next` ボタンを押します。
   
   .. image:: images/mod3-4.png
   |  
#. SSLOでサーバ証明書を書き換える際に利用する　**CA証明書**、**CA鍵** を選択し、**任意の名前** を設定し、:guilabel:`Next` ボタンを押します。
   
   .. image:: images/mod3-5.png
   |  
#. :guilabel:`Finished` ボタンを押します。
   
   .. image:: images/mod3-6.png
