# Our Little World — GitHub Pages 최종본

`index.html`에는 제공해 주신 Supabase Project URL과 anon key가 이미 입력되어 있습니다.

## GitHub 업로드
1. GitHub에서 Repository를 만듭니다.
2. `index.html`을 Repository 최상위에 업로드합니다.
3. Settings → Pages → Deploy from a branch → `main` / `/ (root)` → Save

## Supabase
Project URL: `https://wuoznsowfgntehurrxpx.supabase.co`

사용하는 `pins` 컬럼:
`id`, `type`, `name`, `lat`, `lon`, `image_path`, `seokyung_comment`, `moonhyuk_comment`

Storage bucket: `photos`

## 로그인
서경: `0614`
문혁: `0922`

## 사진
핀 하나당 사진 한 장입니다. 새 사진을 업로드하면 `pins/{핀ID}.jpg`로 기존 사진을 교체합니다.

## 보안
현재 로그인은 브라우저에서 PIN을 확인하는 간단한 잠금 방식이며 Supabase Auth가 아닙니다.
브라우저용 anon key는 소스에 들어갈 수 있지만, Supabase의 RLS(Row Level Security)가 올바르게 설정되어 있어야 데이터가 보호됩니다.
service_role/secret key는 절대 이 파일에 넣지 마세요.
