# Our Little World — GitHub Pages

## 1. 준비
Supabase에서 이미 만든 `pins` 테이블과 `photos` Storage bucket을 사용합니다.

`pins` 테이블은 다음 컬럼을 사용합니다.

- `id` — int4, primary key
- `type` — text
- `name` — text
- `lat` — float4
- `lon` — float4
- `image_path` — text, nullable
- `seokyung_comment` — text, nullable
- `moonhyuk_comment` — text, nullable

## 2. Supabase 값 넣기

`index.html`을 메모장/VS Code 등으로 열고 아래 두 줄을 찾습니다.

```js
const SUPABASE_URL = "YOUR_SUPABASE_URL";
const SUPABASE_ANON_KEY = "YOUR_SUPABASE_ANON_KEY";
```

Supabase Dashboard → Project Settings → API에서

- Project URL
- anon / public key

를 각각 넣습니다.

**service_role key는 절대 넣지 마세요.**

## 3. Storage

Storage bucket 이름은 정확히 `photos`여야 합니다.

사진은 핀마다 아래처럼 한 개의 고정 경로를 사용합니다.

`pins/핀ID.jpg`

새 사진을 올리면 기존 파일을 덮어씁니다.

## 4. GitHub Pages

GitHub에서 새 repository를 만들고 `index.html`을 업로드합니다.

Repository → Settings → Pages → Deploy from a branch → `main` / `/ (root)` → Save

잠시 후 GitHub Pages 주소가 생성됩니다.

## 5. 로그인 PIN

- 서경: `0614`
- 문혁: `0922`

이 로그인은 사이트 화면을 잠그는 간단한 PIN 방식입니다. 실제 보안 인증은 아닙니다.

## 6. 중요: Supabase 권한

현재 버전은 PIN을 브라우저에서 확인하는 방식입니다. 따라서 실제 사용자 인증/보안이 필요한 서비스에는 적합하지 않습니다.

개인적인 여행 기록/생일 사이트 정도로 사용할 경우에는 괜찮지만, 민감한 개인정보나 비공개 자료는 올리지 않는 것을 권장합니다.

또한 Supabase의 `pins`와 `photos`가 실제로 읽기/쓰기 가능하도록 RLS/Storage 정책을 설정해야 합니다.
