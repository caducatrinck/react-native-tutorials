# Gerando Debug Key

-   Abra um terminal com keytool instalado
-   Navegue até a pasta ~/java/sdk/bin

    ![image](./images/imagem1.png)

-   Execute o comando abaixo

    ```
    keytool -genkey -v -keystore debug.keystore -storepass android -alias androiddebugkey -keypass android -keyalg RSA -keysize 2048 -validity 10000
    ```

    ![image](./images/imagem2.png)

-   Mova o arquivo para a pasta do App (myapp/android/app)

    ![image](./images/imagem3.png)
