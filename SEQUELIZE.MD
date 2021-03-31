<div align="center">
    <img src="./assets/logo-small.png" width="200" >

# [SEQUELIZE](https://sequelize.org/?__cf_chl_captcha_tk__=603bf1458f563d44e1cc9d688ae325cce4b3b509-1617206819-0-AWomcFumeUoGRBKbPh9UIAe06NolEfEdJ8bO5LW_NuS_6vOgNm5mGa9b53DH8dhKKpxY5_2L8T6nix7XuKu0cdcLI7xTxx5A5WysRP_6SPZqtfe2R8S_F-4LHW15Y3TBUHkt9cMdS-DDu8u1HPDFV0eixPD_FsbQ4c5ntncn_k1ZWHxaLOSNv367G8vHrRiGZWdIgF7878832n-fYbfKqP5fquPhv9LTRWXTIXy-rmc0n3aHj60b5bxH5DzV7YEpVNFKSdvwHXXMpLNNpH3ens4ESQ0FD2ai5c3l60bUGNvO2XUVbBjho2Wz8oTOB1uWJ_DFQFRgBoAETcKn_PUgoXRa5kI_2u7Xa8eHDzPc5pWLS_92D9c6_nyTzcWl0hjEMVZRu7f0Cg6HJzoKFmdgdZ3ktYOOIKCHn27UR_dCLn3IO3xj7P-NGPFf8LkEI6kQ7yBqkBjVi6nW_dcwFHzhea50CZjvpZ9_rtaj9w_27eT1cUk7ZLUAQZaH9S87dXfH-F6gypwujT6I3ZGhjZ66jahpQavnkd2t3qtfrcAqCW4eQWzQzU-HznrvXcv2e2Er6t14qJp9Z_th2QfGAuKT8r3O3DLMK-QkSyLBYDxMQvsX)

</div>

## Instalaçao

    yarn add sequelize

## Comandos
Criar banco de dados

    yarn sequelize db:create 

### MIGRATIONS
Criar uma migration

    yarn sequelize migration:create --name=create-migration-example

Executar todas as migrations

    yarn sequelize db:migrate

Desfazer a última migration executada

    yarn sequelize db:migrate:undo

Desfazer todas as migrations executadas

    yarn sequelize db:migrate:undo:all

### SEEDS
Criar uma seed

    yarn sequelize seed:generate --name=generate-seed-example

Executar todas as seeds

    yarn sequelize db:seed:all
