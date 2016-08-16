# More HTML Email Snippets

More snippets for faster HTML email coding. Including `preheader table cells`, `VML buttons`, `VML background` and more.

These snippets have incorporated coding techniques that focus on creating non-responsive emails with least quirks possible. *But*, it doesn't mean you can't use it for responsive emails, it may just lack few more codes to fit your coding style. (E.g. it has no `MSO conditionals` on each table/column unlike the [hybrid fluid method](http://webdesign.tutsplus.com/tutorials/creating-a-future-proof-responsive-email-without-media-queries--cms-23919).)

This was specialized for *Straight Arrow Corporation's LexisNexis UK team*. You might find it useful yourself.

## Snippets

To use a snippet, type the trigger codes (listed below in bold) then hit `tab` or `ctrl + enter`.
*Remember*, you can press `tab` / `shift + tab` for speedy navigation from one part of the code to another.


**ehtml** — HTML Email Template
```
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Transitional //EN" "http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd">
<html xmlns="http://www.w3.org/1999/xhtml">
<head>
	<meta http-equiv="content-type" content="text/html; charset=UTF-8" />

	<!--[if !mso]><!-->
	<meta http-equiv="X-UA-Compatible" content="IE=edge" />
	<!--<![endif]-->

	<meta name="viewport" content="width=device-width, initial-scale=1.0" />

	<title></title>

	<!--[if (gte mso 9)|(IE)]>
	<style type="text/css">
		table {border-collapse: collapse;}
	</style>
	<![endif]-->

	<style type="text/css">
		/* Reset and client-specific fixes */


		.ExternalClass { width:100%; }

		.ExternalClass,
		.ExternalClass p,
		.ExternalClass span,
		.ExternalClass font,
		.ExternalClass td,
		.ExternalClass div { line-height:100%; }

		#outlook a { padding:0; }

		body { -webkit-text-size-adjust:100%; }

		table {mso-table-lspace:0pt; mso-table-rspace:0pt;}

		img { height:auto; line-height:100%; outline:none; -ms-interpolation-mode:bicubic; }

		div[style*="margin: 16px 0"] { margin:0 !important; }

	</style>
</head>
<body style="padding:0; Margin:0 !important;">

Content goes here

</body>
</html>
```

**etable** — table
```
<table width="600" align="left" cellpadding="0" cellspacing="0" style="border-spacing:0;">
	<tr>
		<td width="600" align="left" valign="top" style="padding:0;">
			Content goes here
		</td>
	</tr>
</table>
```

**etd** — table cell
```
<td width="600" align="left" valign="top" style="padding:0;">
	Content goes here
</td>
```

**epreheader** — preheader (hidden table cell)
```
<!-- preheader table cell -->
<td style="max-height:0px; max-width:0px; display:none !important; color:#fffffe; font-size:1px; line-height:1px; visibility:hidden; opacity:0; overflow:hidden; mso-hide:all; padding:0;">
	Content goes here
</td>
```

**ea** — link
```
<a href="https://sample.com/" name="" target="_blank" style="color:#0000ee; text-decoration:underline;">This is link</a>
```
*Note: the placeholder `https://sample.com/` was used instead of `#` to prevent some email apps (e.g. Outlook.com) from displaying the "invalid" URLs which could easily break the mail's layout during testing.*

**eimg** — image
```
<img src="path/to/image.gif" alt="" width="" border="0" style="border:0 none; display:block;" />
```

**eaimg** — link + image
```
<a href="https://sample.com/" name="" target="_blank" style="color:#0000ee; text-decoration:underline;">
	<img src="path/to/image.gif" alt="" width="" border="0" style="border:0 none; display:block;" />
</a>
```

**ebtn** — button
```
<!--[if mso]>
	<v:rect xmlns:v="urn:schemas-microsoft-com:vml" xmlns:w="urn:schemas-microsoft-com:office:word" href="https://sample.com/" name="" fillcolor="#ffffff" strokeweight="1px" strokecolor="#000000" style="width:100px; height:20px; v-text-anchor:middle;">
		<w:anchorlock/>
		<center style="color:#000000; font-size:12px; font-family:Arial, 'Helvetica Neue', Helvetica, sans-serif;">This is button</center>
	</v:rect>
<![endif]-->
<a href="https://sample.com/" name="" target="_blank" style="width:100px; display:inline-block; background-color:#ffffff; color:#000000; font-size:12px; line-height:20px; font-family:Arial, 'Helvetica Neue', Helvetica, sans-serif; text-align:center; text-decoration:none; border:1px solid #000000; -webkit-text-size-adjust:none; mso-hide:all;">This is button</a>
```

**erbtn** — round-corners button
```
<!--[if mso]>
	<v:roundrect xmlns:v="urn:schemas-microsoft-com:vml" xmlns:w="urn:schemas-microsoft-com:office:word" href="https://sample.com/" name="" fillcolor="#ffffff" strokeweight="1px" strokecolor="#000000" arcsize="10%" style="width:100px; height:20px; v-text-anchor:middle;">
		<w:anchorlock/>
		<center style="color:#000000; font-size:12px; font-family:Arial, 'Helvetica Neue', Helvetica, sans-serif;">This is button</center>
	</v:roundrect>
<![endif]-->
<a href="https://sample.com/" name="" target="_blank" style="width:100px; display:inline-block; background-color:#ffffff; color:#000000; font-size:12px; line-height:20px; font-family:Arial, 'Helvetica Neue', Helvetica, sans-serif; text-align:center; text-decoration:none; border:1px solid #000000 border-radius:2px; -webkit-text-size-adjust:none; mso-hide:all;">This is button</a>
```

**eimgbtn** — button with image background
```
<!--[if mso]>
	<v:rect xmlns:v="urn:schemas-microsoft-com:vml" xmlns:w="urn:schemas-microsoft-com:office:word" href="https://sample.com/" name="" strokeweight="1px" strokecolor="#000000" style="width:100px; height:20px; v-text-anchor:middle;" fill="t">
		<v:fill type="tile" src="https://i.imgur.com/0xPEf.gif" color="#556270" />
		<w:anchorlock/>
		<center style="color:#000000; font-size:12px; font-family:Arial, 'Helvetica Neue', Helvetica, sans-serif;">This is button</center>
	</v:rect>
<![endif]-->
<a href="https://sample.com/" name="" target="_blank" style="width:100px; line-height:20px; display:inline-block; background-image:url(https://i.imgur.com/0xPEf.gif); background-color:#556270; color:#000000; font-size:12px; font-family:Arial, 'Helvetica Neue', Helvetica, sans-serif; text-align:center; text-decoration:none; border:1px solid #000000; -webkit-text-size-adjust:none; mso-hide:all;">This is button</a>
```

**erimgbtn** — round-corners button with image background
```
<!--[if mso]>
	<v:roundrect xmlns:v="urn:schemas-microsoft-com:vml" xmlns:w="urn:schemas-microsoft-com:office:word" href="https://sample.com/" name="" strokeweight="1px" strokecolor="#000000" arcsize="10%" style="width:100px; height:20px; v-text-anchor:middle;" fill="t">
		<v:fill type="tile" src="https://i.imgur.com/0xPEf.gif" color="#556270" />
		<w:anchorlock/>
		<center style="color:#000000; font-size:12px; font-family:Arial, 'Helvetica Neue', Helvetica, sans-serif;">This is button</center>
	</v:roundrect>
<![endif]-->
<a href="https://sample.com/" name="" target="_blank" style="width:100px; line-height:20px; display:inline-block; background-image:url(https://i.imgur.com/0xPEf.gif); background-color:#556270; color:#000000; font-size:12px; font-family:Arial, 'Helvetica Neue', Helvetica, sans-serif; text-align:center; text-decoration:none; border:1px solid #000000 border-radius:2px; -webkit-text-size-adjust:none; mso-hide:all;">This is button</a>
```

**eimgbg** — image background (table cell)
```
<td background="https://i.imgur.com/YJOX1PC.png" bgcolor="#7bceeb" height="800" width="600" align="left" valign="top" style="padding:0;">
	<!--
	NOTE:
	for full-width table cell:
		remove width attribute from <td> and width style from <v:rect>
		and retain the "mso-width-percent:1000;" style on <v:rect>
	for fixed-width table cell:
		define width attribute on <td> and width style on <v:rect>
		and remove the "mso-width-percent:1000;" style on <v:rect>
	for full-height table cell:
		remove height attribute from <td> and height style from <v:rect>
		and retain the "mso-fit-shape-to-text:true" on <v:textbox>
	for fixed-height table cell:
		define height attribute on <td> and height style on <v:rect>
		and remove the "mso-fit-shape-to-text:true" on <v:textbox>
	-->

	<!--[if gte mso 9]>
	<v:rect xmlns:v="urn:schemas-microsoft-com:vml" fill="true" stroke="false" style="width:600; height:800; mso-width-percent:1000;">
		<v:fill type="tile" src="https://i.imgur.com/YJOX1PC.png" color="#7bceeb" />
		<v:textbox style="mso-fit-shape-to-text:true;" inset="0,0,0,0">
	<![endif]-->
	<div>
		Content goes here
	</div>
	<!--[if gte mso 9]>
		</v:textbox>
	</v:rect>
	<![endif]-->
</td>
```

**etype** — typographical styles
```
color:#000000; font-size:12px; line-height:14px; font-family:Arial, 'Helvetica Neue', Helvetica, sans-serif; text-align:left;
```