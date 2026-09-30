# Домашнее задание — TeamCity

Репозиторий: https://github.com/YangDevOps089/example-teamcity

Инфраструктура: teamcity-server, teamcity-agent, infra-vm (Nexus) на Yandex Cloud.

![](screenshots/10_yandex_cloud_vms.png)
Три виртуалки в Yandex Cloud.

![](screenshots/03_build_steps_conditions.png)
Два шага сборки — Maven (test) и Deploy, у каждого своё условие по ветке.

![](screenshots/04_deploy_step_settings_xml.png)
В шаге Deploy подключён settings.xml с кредами от Nexus.

![](screenshots/05_pomxml_original.png)
pom.xml, поменял адрес Nexus в distributionManagement.

![](screenshots/06_nexus_maven_releases_002.png)
Артефакт после деплоя появился в Nexus.

![](screenshots/08_nexus_maven_releases_002_003.png)
Пришлось поднимать версию в pom.xml, т.к. Nexus не даёт передеплоить ту же версию в release-репозиторий.

![](screenshots/07_feature_branch_build_passed6.png)
Ветка feature/add_reply — добавил метод sayReply() в Welcomer и тест на него, все 6 тестов прошли.

![](screenshots/09_build9_artifacts_jar.png)
После настройки artifact paths (target/*.jar) в сборке появился сам jar-файл.

Дальше смёржил feature/add_reply в master, всё собирается и деплоится нормально.
