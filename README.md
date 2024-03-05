# Clock Widget for Homer
Custom service clock widget for [Homer Dashboard](https://github.com/bastienwirtz/homer)

I use it with [Homer Theme v2](https://github.com/walkxcode/homer-theme)

![изображение](https://github.com/makarbass/Clock-Widget-for-Homer/assets/52400119/baa00d8d-7190-444d-8890-fc4795443749)

## Getting started!

Clone files to your server



Clone [this repo](https://github.com/makarbass/Clock-Widget-for-Homer.git). You can do this by running:

```sh
$ git clone https://github.com/makarbass/Clock-Widget-for-Homer.git
```

Now cd into the newly created folder.

```sh
$ cd Clock-Widget-for-Homer
```

Clone `Clock.vue` file into your Homer services path
```sh
$ cp Clock.vue homer/src/components/services/Clock.vue
```

Add service to `config.yml`

```yml
  - name: "Clock"
    items:
      - name: "Clock"
        logo: "assets/tools/clock.png"
        type: "Clock"
        subtitle: "UTC +3"
```
