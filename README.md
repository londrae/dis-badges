# dis-badges

[![MIT License](https://img.shields.io/badge/license-MIT-green.svg)](https://choosealicense.com/licenses/mit/)
[![](https://disbadges.londra.gq/badge/status/1053616520040816661)](https://github.com/londrae/dis-badges/)

**dis-badges**, Discord aktivitelerinizi GitHub profilinizde sergileyebileceğiniz bir araçtır.<br>
Bu proje, genel kullanıma yönelik olmayan bir geliştirme yapısıdır. Yalnızca `Alpha Testers` projeden yararlanabilir.

## API Kullanımı

#### API temel URL

```
https://disbadges.londra.gq/api/
```

```http
GET /api/badge/:activity/:id
```
> (bkz. [Parametreler](/README.md#parametreler))

## Kullanım

### Parametreler

| Parametre      | Tip         | Gerekli  | Açıklama                                                                |
| :------------- | :---------- | :------: | :---------------------------------------------------------------------- |
| `:activity`     | `string`    | ✅      | İstenen aktivite verisi platformu `status\|playing\|vscode\|spotify`    |
| `:id`           | `string`    | ✅      | Aktivite verileri çağırılacak kullanıcı kimliği                         |

#### İsteğe bağlı parametreler

| Parametre      | Tip         | Gerekli  | Varsayılan | Açıklama                                  |
| :------------- | :---------- | :------: | :--------- | :---------------------------------------- |
| `?iconOnly`     | `boolean`   | ❌      | `false`    | Rozette label etiketi yerine logo görünür |
| `?showUsername` | `boolean`   | ❌      | `false`    | Rozette kullanıcı adını gizle/göster      |
| `?showDiscrim`  | `boolean`   | ❌      | `false`    | Rozette kullanıcı etiketini gizle/göster  |
| `?showIcon`     | `boolean`   | ❌      | `true`     | Rozette konu gizle/göster                 |
| `?style`        | `string`    | ❌      | `flat`     | Rozet stili                               |

**Not:** `?showUsername` ve `?showDiscrim` parametreleri yalnızca `:activity` parametresi `status` değerine sahip olduğunda çalışır.

```http
GET /badge/:activity/:id
GET /badge/:activity/:id?showIcon=false
GET /badge/status/:id?showUsername=true
GET /badge/status/:id?showUsername=true&showIcon=false
```

##### `:activity`

| Değer       | Örnek                                                                                                     |
| :---------- | :-------------------------------------------------------------------------------------------------------- |
| `status`    | ![](https://nocache.londra.workers.dev?url=https://disbadges.londra.gq/badge/status/962684663137181716)   |
| `playing`   | ![](https://nocache.londra.workers.dev?url=https://disbadges.londra.gq/badge/playing/962684663137181716)  |
| `vscode`    | ![](https://nocache.londra.workers.dev?url=https://disbadges.londra.gq/badge/vscode/962684663137181716)   |
| `spotify`   | ![](https://nocache.londra.workers.dev?url=https://disbadges.londra.gq/badge/spotify/962684663137181716)  |

##### `?style`

| Değer           | Örnek                                                                        |
| :-------------- | :--------------------------------------------------------------------------- |
| `plastic`       | ![](https://shields.io/badge/style-plastic-blue?style=plastic)               |
| `flat`          | ![](https://shields.io/badge/style-flat-blue?style=flat)                     |
| `flat-square`   | ![](https://shields.io/badge/style-flat--square-blue?style=flat-square)      |
| `for-the-badge` | ![](https://shields.io/badge/style-for--the--badge-blue?style=for-the-badge) |

## Rozet Değişmiyor Mu?

Rozetin her yenilendiğinde değişmesi için [@londrae](https://github.com/londrae) tarafından geliştirilen [`nocache.londra.workers.dev`](https://nocache.londra.workers.dev) servisini kullanabilirsiniz.

#### Örnek kullanım
```
https://nocache.londra.workers.dev?url=https://disbadges.londra.gq/badge/spotify/962684663137181716
```
> Bu rozet `nocache.londra.workers.dev` servisi sayesinde sayfa her yenilendiğinde yerel cache verilerini temizleyecek ve güncellenecektir.

## Ekran Görüntüleri

<img src="https://media.discordapp.net/attachments/1055791675739471902/1055791782304170034/resim.png" style="width: 550px">

## Yazarlar ve Teşekkür

- [@londrae](https://github.com/londrae) geliştirme için.
- [@efeeozc](https://github.com/efeeozc) dokümanların hazırlanması için.
