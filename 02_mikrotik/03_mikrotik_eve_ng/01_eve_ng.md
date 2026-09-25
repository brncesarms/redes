# Dicas-Mikrotik-EVE-NG

* Fontes:
* <https://youtu.be/cj3qsNsBd2A>
* <https://www.redesbrasil.com/aprenda-a-instalar-e-usar-o-eve-ng-para-emular-roteadores-da-mikrotik/>

## Acesso web:

```bash
admin

```

```bash
eve

```

## Acesso SSH:

```bash
root

```

```bash
eve

```

## 

```bash
mkdir -p /opt/unetlab/addons/qemu/mikrotik-6.49.10

```

```bash
cd /opt/unetlab/addons/qemu/mikrotik-6.49.10

```

```bash
wget https://download.mikrotik.com/routeros/6.49.10/chr-6.49.10.vmdk.zip

```

```bash
unzip chr-6.49.10.vmdk.zip

```

```bash
/opt/qemu/bin/qemu-img convert -f vmdk -O qcow2 chr-6.49.10.vmdk hda.qcow2

```

```bash
rm -rf chr*

```

