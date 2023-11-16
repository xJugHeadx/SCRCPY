# scrcpy (v2.2)

<img src="app/data/icon.svg" width="128" height="128" alt="scrcpy" align="right" />

_pronunciado "**scr**een **c**o**py**"_

Esta aplicación refleja los dispositivos Android (vídeo y audio) conectados a través de
USB o [sobre TCP/IP](doc/connection.md#tcpip-wireless), y permite controlar el
dispositivo con el teclado y el ratón del ordenador. No requiere ningún
_acceso raíz. Funciona en _Linux_, _Windows_ y _macOS_.

![screenshot](assets/screenshot-debian-600.jpg)

Se enfoca en:

 - **ligereza**: nativa, muestra solo la pantalla del dispositivo
 - **rendimiento**: 30~120 fps, dependiendo del dispositivo
 - **calidad**: 1920×1080 o superior
 - **baja latencia**: [35~70ms][baja latencia]
 - **tiempo de inicio bajo**: ~1 segundo para mostrar la primera imagen
 - **no intrusión**: no queda nada instalado en el dispositivo Android
 - **beneficios para el usuario**: sin cuenta, sin anuncios, no se requiere Internet
 - **libertad**: software gratuito y de código abierto

[lowlatency]: https://github.com/Genymobile/scrcpy/pull/646

Sus características incluyen:
 - [reenvío de audio] (doc/audio.md) (Android 11+)
 - [grabación] (doc/recording.md)
 - duplicación con [pantalla del dispositivo Android apagada] (doc/device.md#turn-screen-off)
 - [copiar y pegar](doc/control.md#copiar y pegar) en ambas direcciones
 - [calidad configurable](doc/video.md)
 - [duplicación de cámara] (doc/camera.md) (Android 12+)
 - [duplicación como cámara web (V4L2)](doc/v4l2.md) (solo Linux)
 - [simulación física de teclado/ratón (HID)] (doc/hid-otg.md)
 - [Modo OTG](doc/hid-otg.md#otg)
 - y más…

## Requisitos previos

El dispositivo Android requiere al menos API 21 (Android 5.0).

[Reenvío de audio](doc/audio.md) es compatible con API >= 30 (Android 11+).

Asegúrese de [habilitar la depuración USB] [enable-adb] en su(s) dispositivo(s).

[enable-adb]: https://developer.android.com/studio/debug/dev-options#enable

En algunos dispositivos, también es necesario habilitar [una opción adicional][control] `USB
depuración (Configuración de seguridad)` (este es un elemento diferente de `depuración USB`)
para controlarlo mediante un teclado y un ratón. Es necesario reiniciar el dispositivo una vez.
esta opción está configurada.

[control]: https://github.com/Genymobile/scrcpy/issues/70#issuecomment-373286323

Tenga en cuenta que no se requiere la depuración USB para ejecutar scrcpy en [OTG
modo](doc/hid-otg.md#otg).


## Obtener la aplicación

 - [Linux](doc/linux.md)
 - [Windows](doc/windows.md)
 - [macOS](doc/macos.md)


## Documentación del usuario

La aplicación proporciona muchas funciones y opciones de configuración. Ellos son
documentado en las siguientes páginas:

 - [Connection](doc/connection.md)
 - [Video](doc/video.md)
 - [Audio](doc/audio.md)
 - [Control](doc/control.md)
 - [Device](doc/device.md)
 - [Window](doc/window.md)
 - [Recording](doc/recording.md)
 - [Tunnels](doc/tunnels.md)
 - [HID/OTG](doc/hid-otg.md)
 - [Camera](doc/camera.md)
 - [Video4Linux](doc/v4l2.md)
 - [Shortcuts](doc/shortcuts.md)


## Recursos

 - [Preguntas frecuentes](Preguntas frecuentes.md)
 - [Traducciones][wiki] (no necesariamente actualizado)
 - [Instrucciones de compilación] (doc/build.md)
 - [Desarrolladores] (doc/develop.md)

[wiki]: https://github.com/Genymobile/scrcpy/wiki


## Artículos

- [Presentando scrcpy][artículo-introducción]
- [Scrcpy ahora funciona de forma inalámbrica][artículo-tcpip]
- [Scrcpy 2.0, con audio][artículo-scrcpy2]

[introducción del artículo]: https://blog.rom1v.com/2018/03/introduciendo-scrcpy/
[artículo-tcpip]: https://www.genymotion.com/blog/open-source-project-scrcpy-now-works-wireless/
[artículo-scrcpy2]: https://blog.rom1v.com/2023/03/scrcpy-2-0-with-audio/

## Contacto

Si encuentra un error, lea primero las [Preguntas frecuentes] (FAQ.md) y luego abra un [problema].

[problema]: https://github.com/Genymobile/scrcpy/issues

Para preguntas o discusiones generales, también puede utilizar:

 - Reddit: [`r/scrcpy`](https://www.reddit.com/r/scrcpy)
 - Twitter: [`@scrcpy_app`](https://twitter.com/scrcpy_app)


## Donar

Soy [@rom1v](https://github.com/rom1v), el autor y mantenedor de _scrcpy_.

Si aprecia esta aplicación, puede [apoyar mi código abierto
trabajar][donar]:
 - [Patrocinadores de GitHub](https://github.com/sponsors/rom1v)
 - [Liberapay](https://liberapay.com/rom1v/)
 -[PayPal](https://paypal.me/rom2v)

[donar]: https://blog.rom1v.com/about/#support-my-open-source-work

## Licencia

    Copyright (C) 2018 Genymobile
    Copyright (C) 2018-2023 Romain Vimont

    Licenciado bajo la Licencia Apache, Versión 2.0 (la "Licencia");
    no puede utilizar este archivo excepto de conformidad con la Licencia.
    Puede obtener una copia de la Licencia en

        http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.
