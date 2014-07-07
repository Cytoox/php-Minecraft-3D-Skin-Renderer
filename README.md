php Minecraft 3D Skin Renderer
=====================

Render a 3D view of a Minecraft skin using PHP.

Project first developed by <a href="https://github.com/supermamie/php-Minecraft-3D-skin" target="_blank">supermamie</a>. Later transalated to English by <a href="https://github.com/cajogos/php-Minecraft-3D-Skin-Renderer" target="_blank">cajogos</a>.

My goal is to fix some issues and hopefully create full support for the 1.8 skins.

### Example of URL:
The URL containing most of the options:<br/>
`http://example.com/3d.php?vr=-25&hr=-25&hrh=10&vrla=5&vrra=-2&vrll=-20&vrrl=2&ratio=12&format=png&displayHair=true&headOnly=false&user=Notch`<br/>
Note: The old parameters by supermamie will still work.

With less parameters:<br/>
`http://example.com/3d.php?user=Notch&hrh=-20&aa=true`<br/>
This example will only set the user to Notch, head rotation to -20 and AA (image smoothing) to true. You can add parameters by adding `&<parameter>=<value>` to the end of your URL.

### Parameters
Supermamie's old parameters will still work.

Parameters are now optional, so you can now only add those you need.

- `user` = Minecraft's username for the skin to be rendered. `char by default`
- `vr` = Vertical Rotation `-25 by default`
- `hr` = Horizontal Rotation `35 by default`
- `hrh` = Horizontal Rotation Head `0 by default`
- `vrll` = Vertical Rotation Left Leg `0 by default`
- `vrrl` = Vertical Rotation Right Leg `0 by default`
- `vrla` = Vertical Rotation Left Arm `0 by default`
- `vrra` = Vertical Rotation Right Arm `0 by default`
- `displayHair` = Either or not to display hairs. Set to "false" to NOT display hairs. `true by default`
- `headOnly` = Either or not to display the ONLY the head. Set to "true" to display ONLY the head (and the hair, based on displayHair). `false by default`
- `format` = The format in which the image is to be rendered. PNG ("png") is used by default. Set to "svg" to use a vector version and "base64" for an encoded base64 string of the png image. `png by default`
- `ratio` = The size of the "png" image. The default and minimum value is 2. `12 by default`
- `aa` = Anti-aliasing (Not real AA, fake AA). When set to "true" the image will be smoother. `false by default`

### Changes Made
- Fixed dark blue skins;
- Fixed not working SVG images (Bug in cajogos fork);
- Fixed non-transparent PNG images rendering incorrect (Fix is a bit experimental);
- Made the old parameters by supermamie work again;
- Made 1.8 skins work (still render as the old skin type);
- Added ability to output an encoded base64 string of the image;
- Added optional AA (image smoothing) parameter;
- Made all parameters optional;
- Made Steve the fallback image.