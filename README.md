# dis-badges

[![MIT License](https://img.shields.io/badge/License-MIT-green.svg)](https://choosealicense.com/licenses/mit/)
[![](https://disbadges.londra.gq/badge/status/1053616520040816661)](https://github.com/londrae/dis-badges/)

**dis-badges**, Discord aktivitelerini GitHub profilinizde sergileyebileceğiniz bir araçtır.<br>
Bu proje, genel kullanıma yönelik olmayan bir geliştirme yapısıdır. Yalnızca `Alpha Testers` projeden yararlanabilir.

------

## API Kullanımı

#### API temel URL

```
https://disbadges.londra.gq/api/
```

#### Genel parametreler

| Parametre      | Tip         | Gerekli  | Açıklama                                                                |
| :------------- | :---------- | :------: | :---------------------------------------------------------------------- |
| `activity`     | `string`    | ✅      | İstenen aktivite verisi platformu `status\|playing\|vscode\|spotify`    |
| `id`           | `string`    | ✅      | Aktivite verileri çağırılacak kullanıcı kimliği                         |

```
GET /api/badge/:activity/:id
```
------

## Kullanım

#### Özel parametreler

| Parametre      | Tip         | Gerekli  | Varsayılan | Açıklama                                  |
| :------------- | :---------- | :------: | :--------- | :---------------------------------------- |
| `showUsername` | `boolean`   | ❌      | `false`    | Rozette kullanıcı adını gizle/göster      |
| `showDiscrim`  | `boolean`   | ❌      | `false`    | Rozette kullanıcı etiketini gizle/göster  |
| `showIcon`     | `boolean`   | ❌      | `true`     | Rozette konu gizle/göster                 |

**Not:** `showUsername` ve `showDiscrim` parametreleri yalnızca `activity` parametresi `status` değerine sahip olduğunda çalışır.

**Not:** Özel parametreler `query` olarak yazılmalıdır.

```
/badge/status/:id?showUsername=true
/badge/:activity/:id?showIcon=false
/badge/status/:id?showUsername=true&showIcon=false
```

## Örnekler

![](https://nocache.londra.workers.dev?url=https://disbadges.londra.gq/badge/status/962684663137181716)
```md
![](https://disbadges.londra.gq/badge/status/962684663137181716)
```

![](https://nocache.londra.workers.dev?url=https://disbadges.londra.gq/badge/status/962684663137181716?showUsername=true)
```md
![](https://disbadges.londra.gq/badge/status/962684663137181716?showUsername=true)
```

![](https://nocache.londra.workers.dev?url=https://disbadges.londra.gq/badge/playing/962684663137181716)
```md
![](https://disbadges.londra.gq/badge/playing/962684663137181716)
```

![](https://nocache.londra.workers.dev?url=https://disbadges.londra.gq/badge/vscode/962684663137181716)
```md
![](https://disbadges.londra.gq/badge/vscode/962684663137181716)
```

![](https://nocache.londra.workers.dev?url=https://disbadges.londra.gq/badge/spotify/962684663137181716)
```md
![](https://disbadges.londra.gq/badge/spotify/962684663137181716)
```

## Ekran Görüntüleri

<img src="https://media.discordapp.net/attachments/1055791675739471902/1055791782304170034/resim.png" style="width: 550px">

## Yazarlar ve Teşekkür

- [@londrae](https://github.com/londrae) geliştirme için.
