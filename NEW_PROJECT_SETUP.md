# 鏂伴」鐩枃妗ｉ儴缃叉祦绋?
> 閫傜敤浜庡湪 `wiki-test.hiwonder.com` 鍩熷悕涓嬫柊澧?VitePress 鏂囨。椤圭洰鐨勫満鏅€?> 姣忎釜椤圭洰鐙珛 GitHub 浠撳簱锛岄€氳繃瀹濆 Nginx 鍙嶅悜浠ｇ悊缁熶竴瀵瑰鎻愪緵鏈嶅姟銆?
---

## 鍗犱綅绗﹁鏄?
鏈枃妗ｄ腑浣跨敤浠ヤ笅鍗犱綅绗︼紝浣跨敤鏃惰鍏ㄩ儴鏇挎崲涓哄疄闄呭€硷細

| 鍗犱綅绗?| 鍚箟 | 绀轰緥鍊?|
|--------|------|--------|
| `<椤圭洰鍚?` | URL 璺敱涓殑椤圭洰鏍囪瘑锛堣矾鐢?`/projects/<椤圭洰鍚?/` 涓殑鍊硷級 | `LanderPi`銆乣LeRobot` |
| `<浠撳簱鍚?` | GitHub 浠撳簱鐨勫悕绉帮紙鍙兘涓庨」鐩悕涓嶅悓锛?| `LanderPi-vite`銆乣LeRobot-vite` |

> 鈿狅笍 `<椤圭洰鍚?` 鍜?`<浠撳簱鍚?` 鍙互鐩稿悓涔熷彲浠ヤ笉鍚岋紝浣嗗悓涓€涓」鐩腑鎵€鏈夊湴鏂瑰繀椤讳繚鎸佷竴鑷淬€?
---

## 瀹屾暣娴佺▼

### 绗竴姝ワ細GitHub 鍒涘缓浠撳簱

1. 鍦?GitHub 涓婂垱寤轰竴涓柊浠撳簱锛堝缓璁涓?Public锛?2. 浠撳簱鍚嶈涓?`<浠撳簱鍚?`锛堜緥濡?`LanderPi-vite`锛?3. 涓嶈鍕鹃€?"Initialize this repository"锛堜繚鎸佺┖浠撳簱锛?4. 鏈湴鍏嬮殕绌轰粨搴撳埌浠绘剰鐩綍

```bash
git clone https://github.com/<浣犵殑鐢ㄦ埛鍚?/<浠撳簱鍚?.git
```

---

### 绗簩姝ワ細澶嶅埗妯℃澘椤圭洰

1. 灏嗙幇鏈夌殑 LanderPi-vite 椤圭洰**瀹屾暣澶嶅埗**鍒版柊鍏嬮殕鐨勭┖浠撳簱鐩綍涓?2. 杩涘叆鏂颁粨搴撶洰褰?
---

### 绗笁姝ワ細鏇挎崲鏂囨。鍐呭

1. **鏇挎崲 Markdown 鏂囨。**锛?   - 鍒犻櫎 `docs/docs/` 涓嬬殑鎵€鏈?`.md` 鏂囦欢
   - 鎶婃柊椤圭洰鐨?Markdown 鏂囦欢鏀惧埌 `docs/docs/` 鐩綍涓?
2. **鏇挎崲闈欐€佽祫婧?*锛?   - 鍒犻櫎 `docs/_static/` 涓嬬殑鎵€鏈夊唴瀹?   - 鎶婃柊椤圭洰鐨勫浘鐗囩瓑璧勬簮鏀惧埌 `docs/_static/` 鐩綍涓?
> 馃搶 鏂囦欢鐩綍缁撴瀯淇濇寔 `docs/docs/*.md` 鍜?`docs/_static/**/*` 涓嶅彉锛屽彧鎹㈠唴瀹广€?
---

### 绗洓姝ワ細淇敼閰嶇疆鏂囦欢锛堝叧閿級

闇€瑕佷慨鏀逛互涓?6 涓枃浠朵腑鐨?`<椤圭洰鍚?` 鍜?`<浠撳簱鍚?`锛?
#### 4.1 `docs/.vitepress/config.mts`锛堢 15 琛岋級

```typescript
// 淇敼鍓?const docsBase = normalizeBase(process.env.DOCS_BASE || '/projects/LanderPi/en/latest/')

// 淇敼鍚?const docsBase = normalizeBase(process.env.DOCS_BASE || '/projects/<椤圭洰鍚?/en/latest/')
```

鍚屾椂妫€鏌ョ 641-642 琛岀殑 `title` 鍜?`description`锛?
```typescript
title: '<椤圭洰鍚? Documentation',
description: '<椤圭洰鍚? robot documentation',
```

#### 4.2 `scripts/stage_main_site.mjs`锛堢 10 琛岋級

```javascript
// 淇敼鍓?const targetDir = join(repositoryRoot, 'projects/LanderPi/en/latest')

// 淇敼鍚?const targetDir = join(repositoryRoot, 'projects/<椤圭洰鍚?/en/latest')
```

#### 4.3 鏍圭洰褰?`index.html`

```html
<!DOCTYPE html>
<html>
<head>
  <meta charset="utf-8">
  <meta http-equiv="refresh" content="0;url=/projects/<椤圭洰鍚?/en/latest/docs/<鍏ュ彛鏂囨。鍚?.html">
  <title><椤圭洰鍚? Documentation</title>
</head>
<body>
  <a href="/projects/<椤圭洰鍚?/en/latest/docs/<鍏ュ彛鏂囨。鍚?.html">Click here if you are not redirected automatically.</a>
</body>
</html>
```

> 鈿狅笍 `<鍏ュ彛鏂囨。鍚?` 鏄?`docs/docs/` 涓嬬殑绗竴涓枃妗ｅ悕锛堜笉鍚?`.md` 鍚庣紑锛夛紝渚嬪 `1_LanderPi_User_Manual`銆?
#### 4.4 `docs/index.md`锛堢 3 琛岋級

```markdown
---
layout: page-redirect
redirectTo: /docs/<鍏ュ彛鏂囨。鍚?.html
---
```

> 杩欓噷鏄浉瀵逛簬 `base` 鐨勮矾寰勶紝涓嶇敤鍔?`/projects/<椤圭洰鍚?/en/latest/` 鍓嶇紑銆?
#### 4.5 `docs/docs/index.md`锛堢 3 琛岋級

鍚屼笂锛?
```markdown
---
layout: page-redirect
redirectTo: /docs/<鍏ュ彛鏂囨。鍚?.html
---
```

#### 4.6 `README.md`锛堝彲閫夛級

鏇存柊椤圭洰鎻忚堪锛?
```markdown
# <椤圭洰鍚? Documentation

This repository contains the <椤圭洰鍚? VitePress documentation site.
```

---

### 绗簲姝ワ細鏈湴鏋勫缓楠岃瘉

鍦ㄤ粨搴撴牴鐩綍鎵ц锛?
```bash
# 1. 瀹夎渚濊禆锛堥娆￠渶瑕侊級
npm ci

# 2. 鏋勫缓鏂囨。
npm run docs:build

# 3. 鏁寸悊鏋勫缓浜х墿
npm run docs:stage-main
```

鏋勫缓瀹屾垚鍚庯紝妫€鏌?`projects/<椤圭洰鍚?/en/latest/` 鐩綍锛?
- 搴旇鏈?`docs/*.html`锛堟瘡涓?md 瀵瑰簲涓€涓?html锛?- 搴旇鏈?`assets/`锛堝寘鍚?CSS銆丣S銆佸浘鐗囷級
- 搴旇鏈?`index.html`

**鍏抽敭妫€鏌?*锛氭墦寮€ `projects/<椤圭洰鍚?/en/latest/index.html`锛岀‘璁ゅ叾涓殑 CSS 璺緞涓猴細
```
/projects/<椤圭洰鍚?/en/latest/assets/xxx.css
```

濡傛灉璺緞涓嶅锛岃鏄?`config.mts` 鐨?`base` 閰嶇疆鏈夎銆?
---

### 绗叚姝ワ細鎻愪氦骞舵帹閫佸埌 GitHub

```bash
# 1. 娣诲姞鏂囦欢锛堟敞鎰忎笉瑕佹彁浜?node_modules銆乨ocs/.vitepress/dist 绛夛級
git add projects/ index.html .nojekyll .gitignore package.json package-lock.json scripts/ docs/ .vitepress/

# 2. 绠€鍖栨彁浜わ紙鎺ㄨ崘锛?git add -A
# 浣嗚纭繚 .gitignore 姝ｇ‘

# 3. 鎻愪氦
git commit -m "init: <椤圭洰鍚? 鏂囨。鍒濆鍖?

# 4. 鎺ㄩ€?git push origin main
```

> 馃搶 `.gitignore` 搴斿寘鍚?`node_modules/`锛屼絾 `docs/`銆乣scripts/` 绛夋簮鐮佸彲浠ヤ繚鐣欙紙鍙栧喅浜庝綘甯屾湜浠撳簱鍖呭惈浠€涔堬級銆?> **蹇呴』鎻愪氦**锛歚projects/`銆乣index.html`銆乣.nojekyll`锛圙itHub Pages 鐩存帴鏈嶅姟杩欎簺闈欐€佹枃浠讹級銆?
---

### 绗竷姝ワ細閰嶇疆 GitHub Pages

1. 鎵撳紑 GitHub 浠撳簱 鈫?**Settings** 鈫?**Pages**
2. **Source**: `Deploy from a branch`
3. **Branch**: `main` / `root`
4. **涓嶈缁戝畾鑷畾涔夊煙鍚?*锛圕ustom domain 鐣欑┖锛?
绛夊緟鍑犲垎閽燂紝楠岃瘉 GitHub Pages 鐩磋繛鏄惁鍙闂細
```
https://<浣犵殑GitHub鐢ㄦ埛鍚?.github.io/<浠撳簱鍚?/projects/<椤圭洰鍚?/en/latest/
```

> 渚嬪锛歚https://hiwonder-docs.github.io/LanderPi-vite/projects/LanderPi/en/latest/`

濡傛灉 CSS 鏍峰紡姝ｅ父锛岃鏄?GitHub Pages 閰嶇疆鎴愬姛銆?
---

### 绗叓姝ワ細閰嶇疆瀹濆 Nginx 鍙嶅悜浠ｇ悊

1. 鐧诲綍瀹濆闈㈡澘
2. 鎵惧埌 `wiki-test.hiwonder.com` 绔欑偣 鈫?**璁剧疆** 鈫?**閰嶇疆鏂囦欢**
3. 鍦?`server {}` 鍧楀唴杩藉姞涓€鏉?location 瑙勫垯锛?
```nginx
# <椤圭洰鍚?
location ^~ /projects/<椤圭洰鍚?/ {
    proxy_pass https://hiwonder-docs.github.io/<浠撳簱鍚?/projects/<椤圭洰鍚?/;
    proxy_set_header Host hiwonder-docs.github.io;
    proxy_set_header X-Real-IP $remote_addr;
    proxy_set_header X-Forwarded-For $proxy_add_x_forwarded_for;
    proxy_set_header X-Forwarded-Proto $scheme;
    proxy_ssl_server_name on;
}
```

浠?LanderPi 涓轰緥锛?
```nginx
# LanderPi
location ^~ /projects/LanderPi/ {
    proxy_pass https://hiwonder-docs.github.io/LanderPi-vite/projects/LanderPi/;
    proxy_set_header Host hiwonder-docs.github.io;
    proxy_set_header X-Real-IP $remote_addr;
    proxy_set_header X-Forwarded-For $proxy_add_x_forwarded_for;
    proxy_set_header X-Forwarded-Proto $scheme;
    proxy_ssl_server_name on;
}
```

4. **淇濆瓨骞堕噸杞?Nginx**

> 鈿狅笍 **甯歌閿欒**锛歚proxy_pass` 鍚庨潰**涓嶈鍔犲弽寮曞彿**锛佺洿鎺ュ啓 URL锛屼互鍒嗗彿 `;` 缁撳熬銆?
---

### 绗節姝ワ細楠岃瘉璁块棶

娴忚鍣ㄨ闂細
```
https://wiki-test.hiwonder.com/projects/<椤圭洰鍚?/en/latest/
```

搴旇嚜鍔ㄨ烦杞埌鏂囨。棣栭〉銆傚鏋滄牱寮忔甯搞€佸浘鐗囨樉绀烘甯革紝閮ㄧ讲鎴愬姛銆?
---

## 蹇€熸鏌ユ竻鍗?
鎸夋娓呭崟閫愰」纭锛?
- [ ] GitHub 宸插垱寤虹┖浠撳簱 `<浠撳簱鍚?`
- [ ] 鏈湴浠撳簱宸插鍒舵ā鏉块」鐩?- [ ] `docs/docs/` 涓嬬殑 Markdown 鏂囦欢宸叉浛鎹负鏂伴」鐩唴瀹?- [ ] `docs/_static/` 涓嬬殑闈欐€佽祫婧愬凡鏇挎崲
- [ ] `docs/.vitepress/config.mts` 鐨?`base` 宸叉敼涓?`/projects/<椤圭洰鍚?/en/latest/`
- [ ] `docs/.vitepress/config.mts` 鐨?`title`銆乣description` 宸叉洿鏂?- [ ] `scripts/stage_main_site.mjs` 鐨?`targetDir` 宸叉敼涓?`projects/<椤圭洰鍚?/en/latest`
- [ ] 鏍圭洰褰?`index.html` 閲嶅畾鍚戣矾寰勫凡鏇存柊
- [ ] `docs/index.md` 鐨?`redirectTo` 宸叉洿鏂?- [ ] `docs/docs/index.md` 鐨?`redirectTo` 宸叉洿鏂?- [ ] `npm run docs:build` 鎵ц鎴愬姛
- [ ] `npm run docs:stage-main` 鎵ц鎴愬姛
- [ ] `projects/<椤圭洰鍚?/en/latest/` 鐩綍涓嬫湁 `docs/`銆乣assets/`銆乣index.html`
- [ ] 鐢熸垚鐨?HTML 涓?CSS 璺緞涓?`/projects/<椤圭洰鍚?/en/latest/assets/xxx.css`
- [ ] 宸叉彁浜ゅ苟鎺ㄩ€佸埌 GitHub
- [ ] GitHub Pages Source 璁句负 `main` / `root`
- [ ] GitHub Pages 鏈粦瀹氳嚜瀹氫箟鍩熷悕
- [ ] GitHub Pages 鐩磋繛璁块棶姝ｅ父锛坄https://<鐢ㄦ埛鍚?.github.io/<浠撳簱鍚?/...`锛?- [ ] 瀹濆 Nginx 宸叉坊鍔?`location ^~ /projects/<椤圭洰鍚?/` 瑙勫垯
- [ ] Nginx 瑙勫垯涓?`proxy_pass` 鏃犲弽寮曞彿
- [ ] Nginx 瑙勫垯涓?`proxy_pass` 鐨?`<浠撳簱鍚?` 涓?git remote 涓€鑷达紙鎵ц `git remote -v` 纭锛岄€氬父甯?`-vite` 鍚庣紑锛?- [ ] Nginx 宸查噸杞?- [ ] `https://wiki-test.hiwonder.com/projects/<椤圭洰鍚?/en/latest/` 璁块棶姝ｅ父

---

## 甯歌闂

### Q1: 璁块棶鎶?502 Bad Gateway

**鍘熷洜**锛歂ginx 閰嶇疆閿欒锛屽父瑙佹湁涓や釜鍧戯細

1. **鍙嶅紩鍙烽棶棰?*锛氫粠鏂囨。澶嶅埗浠ｇ爜鏃讹紝`proxy_pass` URL 琚弽寮曞彿鍖呰９鈥斺€?*杩欐槸鏈€甯歌鍘熷洜**
2. **浠撳簱鍚嶄笉鍖归厤**锛歚<浠撳簱鍚?`锛圙itHub 浠撳簱鍚嶏紝閫氬父甯?`-vite` 鍚庣紑锛変笌 `<椤圭洰鍚?`锛圲RL 璺敱锛屼笉甯﹀悗缂€锛夋贩娣?
**妫€鏌?*锛?1. `proxy_pass` 鍚庨潰鏄惁鏈夊浣欑殑鍙嶅紩鍙凤紙\`锛?2. `proxy_pass` 鐨?URL 鏄惁姝ｇ‘锛歚https://hiwonder-docs.github.io/<浠撳簱鍚?/projects/<椤圭洰鍚?/`
3. `<浠撳簱鍚?` 鏄惁涓?`git remote -v` 涓殑 origin 涓€鑷达紙閫氬父甯?`-vite` 鍚庣紑锛?4. 鐩存帴璁块棶 `https://<鐢ㄦ埛鍚?.github.io/<浠撳簱鍚?/projects/<椤圭洰鍚?/en/latest/` 楠岃瘉 GitHub Pages 鏄惁鍙闂?
**姝ｇ‘鍐欐硶**锛?```nginx
# 鉁?鏃犲弽寮曞彿 + 浠撳簱鍚嶅甫 -vite 鍚庣紑锛堝鏋滀粨搴撳悕鏈夊悗缂€锛?proxy_pass https://hiwonder-docs.github.io/<浠撳簱鍚?/projects/<椤圭洰鍚?/;
```

**閿欒鍐欐硶**锛堜細 502锛夛細
```nginx
# 鉂?鏈夊弽寮曞彿
proxy_pass `https://hiwonder-docs.github.io/<浠撳簱鍚?/projects/<椤圭洰鍚?/;`

# 鉂?浠撳簱鍚嶇己 -vite 鍚庣紑锛堝亣璁句粨搴撳悕鏄?xxx-vite锛?proxy_pass https://hiwonder-docs.github.io/<椤圭洰鍚?/projects/<椤圭洰鍚?/;
```

**璁板繂鍙ｈ瘈**锛氶」鐩悕涓嶅甫 `-vite`锛屼粨搴撳悕甯?`-vite`锛孨ginx 鐨?`proxy_pass` 閲屼袱涓悕瀛椾笉瑕佹悶鍙嶃€?
### Q2: 椤甸潰鑳芥墦寮€浣?CSS 涓㈠け

**鍘熷洜**锛歚base` 閰嶇疆閿欒锛屾垨鏋勫缓浜х墿鏈帹閫佸埌 GitHub銆?
**妫€鏌?*锛?1. 鎵撳紑 `projects/<椤圭洰鍚?/en/latest/index.html`锛岀湅 CSS 璺緞鏄惁涓?`/projects/<椤圭洰鍚?/en/latest/assets/xxx.css`
2. 纭 `config.mts` 鐨?`base` 涓?`/projects/<椤圭洰鍚?/en/latest/`
3. 纭 `projects/` 鐩綍宸叉彁浜ゅ埌 GitHub
4. 娴忚鍣?F12 鈫?Network 鈫?鐪?CSS 璇锋眰杩斿洖浠€涔堢姸鎬?
### Q3: 璁块棶鎶?500 鏈嶅姟鍣ㄥ紓甯?
**鍘熷洜**锛氳姹傝 PHP 鎷︽埅銆?
**瑙ｅ喅**锛歭ocation 鍓嶇紑鍔?`^~`锛?```nginx
location ^~ /projects/<椤圭洰鍚?/ {
```

### Q4: 璁块棶鎶ュ煙鍚嶅凡鍗犵敤

**鍘熷洜**锛氬彟涓€涓?GitHub 浠撳簱杩樼粦鐫€ `wiki-test.hiwonder.com`銆?
**瑙ｅ喅**锛氬湪璇ヤ粨搴?Settings 鈫?Pages 鈫?Custom domain 鈫?Remove銆?
### Q5: 鏋勫缓浜х墿璺緞涓嶅锛堢敓鎴愪簡 `projects/` 鑰屼笉鏄?`projects/<椤圭洰鍚?/en/latest/`锛?
**鍘熷洜**锛歚stage_main_site.mjs` 鐨?`targetDir` 鏈洿鏂般€?
**瑙ｅ喅**锛氱‘璁ょ 10 琛屼负锛?```javascript
const targetDir = join(repositoryRoot, 'projects/<椤圭洰鍚?/en/latest')
```

---

## 鏂囦欢缁撴瀯鍙傝€?
瀹屾暣鐨勯」鐩洰褰曠粨鏋勫涓嬶細

```
<浠撳簱鍚?/
鈹溾攢鈹€ docs/
鈹?  鈹溾攢鈹€ .vitepress/
鈹?  鈹?  鈹溾攢鈹€ config.mts              鈫?VitePress 閰嶇疆锛堟敼 base锛?鈹?  鈹?  鈹斺攢鈹€ autoSidebar.mts         鈫?渚ц竟鏍忚嚜鍔ㄧ敓鎴愶紙涓€鑸笉鐢ㄦ敼锛?鈹?  鈹溾攢鈹€ docs/                       鈫?Markdown 鏂囨。锛堟浛鎹㈠唴瀹癸級
鈹?  鈹?  鈹溾攢鈹€ 1_xxx.md
鈹?  鈹?  鈹溾攢鈹€ 2_xxx.md
鈹?  鈹?  鈹斺攢鈹€ index.md
鈹?  鈹溾攢鈹€ _static/                    鈫?闈欐€佽祫婧愶紙鏇挎崲鍐呭锛?鈹?  鈹?  鈹斺攢鈹€ media/
鈹?  鈹溾攢鈹€ public/
鈹?  鈹?  鈹溾攢鈹€ favicon.ico
鈹?  鈹?  鈹斺攢鈹€ e-logo.png
鈹?  鈹斺攢鈹€ index.md                    鈫?棣栭〉閲嶅畾鍚戯紙鏀?redirectTo锛?鈹溾攢鈹€ scripts/
鈹?  鈹斺攢鈹€ stage_main_site.mjs         鈫?鏋勫缓鑴氭湰锛堟敼 targetDir锛?鈹溾攢鈹€ projects/                       鈫?鏋勫缓浜х墿锛堣嚜鍔ㄧ敓鎴愶紝闇€鎻愪氦锛?鈹?  鈹斺攢鈹€ <椤圭洰鍚?/
鈹?      鈹斺攢鈹€ en/
鈹?          鈹斺攢鈹€ latest/
鈹?              鈹溾攢鈹€ assets/
鈹?              鈹溾攢鈹€ docs/
鈹?              鈹?  鈹斺攢鈹€ *.html
鈹?              鈹溾攢鈹€ index.html
鈹?              鈹溾攢鈹€ 404.html
鈹?              鈹溾攢鈹€ favicon.ico
鈹?              鈹斺攢鈹€ ...
鈹溾攢鈹€ .nojekyll                       鈫?绌烘枃浠讹紝闃叉 GitHub Pages 蹇界暐 _ 寮€澶存枃浠?鈹溾攢鈹€ .gitignore
鈹溾攢鈹€ index.html                      鈫?鏍圭洰褰曢噸瀹氬悜锛堟敼 URL锛?鈹溾攢鈹€ package.json
鈹溾攢鈹€ package-lock.json
鈹斺攢鈹€ README.md
```

---

## 鍏抽敭閰嶇疆椤归€熸煡琛?
| 鏂囦欢 | 閰嶇疆椤?| 鍊?|
|------|--------|-----|
| `docs/.vitepress/config.mts` | `base` | `/projects/<椤圭洰鍚?/en/latest/` |
| `scripts/stage_main_site.mjs` | `targetDir` | `projects/<椤圭洰鍚?/en/latest` |
| 鏍圭洰褰?`index.html` | `meta refresh` | `/projects/<椤圭洰鍚?/en/latest/docs/<鍏ュ彛>.html` |
| `docs/index.md` | `redirectTo` | `/docs/<鍏ュ彛>.html` |
| `docs/docs/index.md` | `redirectTo` | `/docs/<鍏ュ彛>.html` |
| Nginx `location` | 鍖归厤璺緞 | `^~ /projects/<椤圭洰鍚?/` |
| Nginx `proxy_pass` | 涓婃父鍦板潃 | `https://hiwonder-docs.github.io/<浠撳簱鍚?/projects/<椤圭洰鍚?/` |
