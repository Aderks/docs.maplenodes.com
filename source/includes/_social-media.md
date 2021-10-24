# Social Media Services

Call                                                      | Description
----------------------------------------------------------|---------------------------------
[4chanBoards](#4chanboards)                               | All available 4chan boards.
[4chanThreadViewer](#4chanthreadviewer)                   | 4chan thread from a specified board.
[4chanThreadViewerPrice](#4chanthreadviewerprice)         | 4chan thread from a specified board with pricing information of a specified crypto ticker based off the original post creation time.
[4chanThreads](#4chanthreads)                             | 4chan threads from a specified board.
[TwitterSearch](#twittersearch)                           | Searches Twitter for tweets based on user inputs. Search is limited to 1 week history.




## 4chanBoards

All available 4chan boards.


### Request Parameters

> Sample Request

```shell
curl -H "Accept: application/json" -H "Content-Type: application/json" -d '[]' https://api.maplenodes.com/xrs/4chanBoards
```

<code class="api-call">4chanBoards</code>

This call does not take parameters.


### Response

<aside class="success">
200 OK
</aside>

> Sample 200 Response

```shell
{
  "boards": [
    {
      "board": "3",
      "title": "3DCG",
      "ws_board": 1,
      "per_page": 15,
      "pages": 10,
      "max_filesize": 4194304,
      "max_webm_filesize": 3145728,
      "max_comment_chars": 2000,
      "max_webm_duration": 120,
      "bump_limit": 310,
      "image_limit": 150,
      "cooldowns": {
        "threads": 600,
        "replies": 60,
        "images": 60
      },
      "meta_description": "&quot;/3/ - 3DCG&quot; is 4chan's board for 3D modeling and imagery.",
      "is_archived": 1
    },
    {
      "board": "a",
      "title": "Anime & Manga",
      "ws_board": 1,
      "per_page": 15,
      "pages": 10,
      "max_filesize": 4194304,
      "max_webm_filesize": 3145728,
      "max_comment_chars": 2000,
      "max_webm_duration": 120,
      "bump_limit": 500,
      "image_limit": 300,
      "cooldowns": {
        "threads": 600,
        "replies": 60,
        "images": 60
      },
      "meta_description": "&quot;/a/ - Anime &amp; Manga&quot; is 4chan's imageboard dedicated to the discussion of Japanese animation and manga.",
      "spoilers": 1,
      "custom_spoilers": 1,
      "is_archived": 1
    },
    {
      "board": "aco",
      "title": "Adult Cartoons",
      "ws_board": 0,
      "per_page": 15,
      "pages": 10,
      "max_filesize": 4194304,
      "max_webm_filesize": 3145728,
      "max_comment_chars": 2000,
      "max_webm_duration": 120,
      "bump_limit": 300,
      "image_limit": 300,
      "cooldowns": {
        "threads": 600,
        "replies": 60,
        "images": 30
      },
      "meta_description": "&quot;/aco/ - Adult Cartoons&quot; is 4chan's imageboard for posting western-styled adult cartoon artwork.",
      "is_archived": 1
    },
    {
      "board": "adv",
      "title": "Advice",
      "ws_board": 1,
      "per_page": 15,
      "pages": 10,
      "max_filesize": 4194304,
      "max_webm_filesize": 3145728,
      "max_comment_chars": 2000,
      "max_webm_duration": 120,
      "bump_limit": 310,
      "image_limit": 150,
      "cooldowns": {
        "threads": 600,
        "replies": 60,
        "images": 60
      },
      "meta_description": "&quot;/adv/ - Advice&quot; is 4chan's board for giving and receiving advice. ",
      "is_archived": 1
    },
    {
      "board": "an",
      "title": "Animals & Nature",
      "ws_board": 1,
      "per_page": 15,
      "pages": 10,
      "max_filesize": 4194304,
      "max_webm_filesize": 3145728,
      "max_comment_chars": 2000,
      "max_webm_duration": 120,
      "bump_limit": 310,
      "image_limit": 150,
      "cooldowns": {
        "threads": 600,
        "replies": 60,
        "images": 60
      },
      "meta_description": "&quot;/an/ - Animals &amp; Nature&quot; is 4chan's imageboard for posting pictures of animals, pets, and nature.",
      "is_archived": 1
    },
    {
      "board": "asp",
      "title": "Alternative Sports & Wrestling",
      "ws_board": 1,
      "per_page": 15,
      "pages": 10,
      "max_filesize": 4194304,
      "max_webm_filesize": 3145728,
      "max_comment_chars": 2000,
      "max_webm_duration": 120,
      "bump_limit": 310,
      "image_limit": 150,
      "cooldowns": {
        "threads": 600,
        "replies": 60,
        "images": 60
      },
      "meta_description": "&quot;/asp/ - Alternative Sports &amp; Wrestling&quot; is 4chan's imageboard for the discussion of alternative and extreme sports such as wrestling and paintball.",
      "is_archived": 1
    },
    {
      "board": "b",
      "title": "Random",
      "ws_board": 0,
      "per_page": 15,
      "pages": 10,
      "max_filesize": 2097152,
      "max_webm_filesize": 2097152,
      "max_comment_chars": 2000,
      "max_webm_duration": 120,
      "bump_limit": 300,
      "image_limit": 150,
      "cooldowns": {
        "threads": 90,
        "replies": 30,
        "images": 30
      },
      "meta_description": "&quot;/b/ - Random&quot; is the birthplace of Anonymous, and where people go to discuss random topics and create memes on 4chan.",
      "forced_anon": 1
    },
    {
      "board": "bant",
      "title": "International/Random",
      "ws_board": 0,
      "per_page": 15,
      "pages": 10,
      "max_filesize": 2097152,
      "max_webm_filesize": 2097152,
      "max_comment_chars": 2000,
      "max_webm_duration": 120,
      "bump_limit": 300,
      "image_limit": 150,
      "cooldowns": {
        "threads": 60,
        "replies": 15,
        "images": 15
      },
      "meta_description": "&quot;/bant/ - International/Random&quot; is 4chan's international hanging out board, where you can have fun with Anonymous all over the world.",
      "user_ids": 1,
      "country_flags": 1
    },
    {
      "board": "biz",
      "title": "Business & Finance",
      "ws_board": 1,
      "per_page": 15,
      "pages": 10,
      "max_filesize": 4194304,
      "max_webm_filesize": 3145728,
      "max_comment_chars": 2000,
      "max_webm_duration": 120,
      "bump_limit": 310,
      "image_limit": 150,
      "cooldowns": {
        "threads": 600,
        "replies": 60,
        "images": 60
      },
      "meta_description": "&quot;/biz/ - Business &amp; Finance&quot; is 4chan's imageboard for the discussion of business and finance, and cryptocurrencies such as Bitcoin and Dogecoin.",
      "user_ids": 1,
      "is_archived": 1
    },
    {
      "board": "c",
      "title": "Anime/Cute",
      "ws_board": 1,
      "per_page": 15,
      "pages": 10,
      "max_filesize": 4194304,
      "max_webm_filesize": 3145728,
      "max_comment_chars": 2000,
      "max_webm_duration": 120,
      "bump_limit": 310,
      "image_limit": 150,
      "cooldowns": {
        "threads": 600,
        "replies": 60,
        "images": 60
      },
      "meta_description": "&quot;/c/ - Anime/Cute&quot; is 4chan's imageboard for cute and moe anime images.",
      "is_archived": 1
    },
    {
      "board": "cgl",
      "title": "Cosplay & EGL",
      "ws_board": 1,
      "per_page": 15,
      "pages": 10,
      "max_filesize": 4194304,
      "max_webm_filesize": 3145728,
      "max_comment_chars": 2000,
      "max_webm_duration": 120,
      "bump_limit": 310,
      "image_limit": 150,
      "cooldowns": {
        "threads": 600,
        "replies": 60,
        "images": 60
      },
      "meta_description": "&quot;/cgl/ - Cosplay &amp; EGL&quot; is 4chan's imageboard for the discussion of cosplay, elegant gothic lolita (EGL), and anime conventions.",
      "is_archived": 1
    },
    {
      "board": "ck",
      "title": "Food & Cooking",
      "ws_board": 1,
      "per_page": 15,
      "pages": 10,
      "max_filesize": 4194304,
      "max_webm_filesize": 3145728,
      "max_comment_chars": 2000,
      "max_webm_duration": 120,
      "bump_limit": 310,
      "image_limit": 150,
      "cooldowns": {
        "threads": 600,
        "replies": 60,
        "images": 60
      },
      "meta_description": "&quot;/ck/ - Food &amp; Cooking&quot; is 4chan's imageboard for food pictures and cooking recipes.",
      "is_archived": 1
    },
    {
      "board": "cm",
      "title": "Cute/Male",
      "ws_board": 1,
      "per_page": 15,
      "pages": 10,
      "max_filesize": 4194304,
      "max_webm_filesize": 3145728,
      "max_comment_chars": 2000,
      "max_webm_duration": 120,
      "bump_limit": 310,
      "image_limit": 150,
      "cooldowns": {
        "threads": 600,
        "replies": 60,
        "images": 60
      },
      "meta_description": "&quot;/cm/ - Cute/Male&quot; is 4chan's imageboard for posting pictures of cute anime males.",
      "is_archived": 1
    },
    {
      "board": "co",
      "title": "Comics & Cartoons",
      "ws_board": 1,
      "per_page": 15,
      "pages": 10,
      "max_filesize": 4194304,
      "max_webm_filesize": 3145728,
      "max_comment_chars": 2000,
      "max_webm_duration": 120,
      "bump_limit": 500,
      "image_limit": 300,
      "cooldowns": {
        "threads": 600,
        "replies": 60,
        "images": 60
      },
      "meta_description": "&quot;/co/ - Comics &amp; Cartoons&quot; is 4chan's imageboard dedicated to the discussion of Western cartoons and comics.",
      "spoilers": 1,
      "custom_spoilers": 5,
      "is_archived": 1
    },
    {
      "board": "d",
      "title": "Hentai/Alternative",
      "ws_board": 0,
      "per_page": 15,
      "pages": 10,
      "max_filesize": 4194304,
      "max_webm_filesize": 3145728,
      "max_comment_chars": 2000,
      "max_webm_duration": 120,
      "bump_limit": 300,
      "image_limit": 300,
      "cooldowns": {
        "threads": 600,
        "replies": 60,
        "images": 30
      },
      "meta_description": "&quot;/d/ - Hentai/Alternative&quot; is 4chan's imageboard for alternative hentai images.",
      "is_archived": 1
    },
    {
      "board": "diy",
      "title": "Do It Yourself",
      "ws_board": 1,
      "per_page": 15,
      "pages": 10,
      "max_filesize": 4194304,
      "max_webm_filesize": 3145728,
      "max_comment_chars": 2000,
      "max_webm_duration": 120,
      "bump_limit": 310,
      "image_limit": 150,
      "cooldowns": {
        "threads": 600,
        "replies": 60,
        "images": 60
      },
      "meta_description": "&quot;/diy/ - Do It Yourself&quot; is 4chan's imageboard for DIY/do it yourself projects, home improvement, and makers.",
      "is_archived": 1
    },
    {
      "board": "e",
      "title": "Ecchi",
      "ws_board": 0,
      "per_page": 15,
      "pages": 10,
      "max_filesize": 4194304,
      "max_webm_filesize": 3145728,
      "max_comment_chars": 2000,
      "max_webm_duration": 120,
      "bump_limit": 300,
      "image_limit": 300,
      "cooldowns": {
        "threads": 600,
        "replies": 60,
        "images": 30
      },
      "meta_description": "&quot;/e/ - Ecchi&quot; is 4chan's imageboard for suggestive (ecchi) hentai images.",
      "is_archived": 1
    },
    {
      "board": "f",
      "title": "Flash",
      "ws_board": 0,
      "per_page": 30,
      "pages": 1,
      "max_filesize": 10485760,
      "max_webm_filesize": 3145728,
      "max_comment_chars": 2000,
      "max_webm_duration": 120,
      "bump_limit": 300,
      "image_limit": 300,
      "cooldowns": {
        "threads": 600,
        "replies": 60,
        "images": 30
      },
      "meta_description": "&quot;/f/ - Flash&quot; is 4chan's upload board for sharing Adobe Flash files (SWFs)."
    },
    {
      "board": "fa",
      "title": "Fashion",
      "ws_board": 1,
      "per_page": 15,
      "pages": 10,
      "max_filesize": 4194304,
      "max_webm_filesize": 3145728,
      "max_comment_chars": 2000,
      "max_webm_duration": 120,
      "bump_limit": 310,
      "image_limit": 150,
      "cooldowns": {
        "threads": 600,
        "replies": 60,
        "images": 60
      },
      "meta_description": "&quot;/fa/ - Fashion&quot; is 4chan's imageboard for images and discussion relating to fashion and apparel.",
      "is_archived": 1
    },
    {
      "board": "fit",
      "title": "Fitness",
      "ws_board": 1,
      "per_page": 15,
      "pages": 10,
      "max_filesize": 4194304,
      "max_webm_filesize": 3145728,
      "max_comment_chars": 2000,
      "max_webm_duration": 120,
      "bump_limit": 310,
      "image_limit": 150,
      "cooldowns": {
        "threads": 600,
        "replies": 60,
        "images": 60
      },
      "meta_description": "&quot;/fit/ - Fitness&quot; is 4chan's imageboard for weightlifting, health, and fitness.",
      "is_archived": 1
    },
    {
      "board": "g",
      "title": "Technology",
      "ws_board": 1,
      "per_page": 15,
      "pages": 10,
      "max_filesize": 4194304,
      "max_webm_filesize": 3145728,
      "max_comment_chars": 2000,
      "max_webm_duration": 120,
      "bump_limit": 310,
      "image_limit": 150,
      "cooldowns": {
        "threads": 600,
        "replies": 60,
        "images": 60
      },
      "meta_description": "&quot;/g/ - Technology&quot; is 4chan's imageboard for discussing computer hardware and software, programming, and general technology.",
      "is_archived": 1,
      "code_tags": 1
    },
    {
      "board": "gd",
      "title": "Graphic Design",
      "ws_board": 1,
      "per_page": 15,
      "pages": 10,
      "max_filesize": 8388608,
      "max_webm_filesize": 3145728,
      "max_comment_chars": 2000,
      "max_webm_duration": 120,
      "bump_limit": 310,
      "image_limit": 150,
      "cooldowns": {
        "threads": 600,
        "replies": 60,
        "images": 60
      },
      "meta_description": "&quot;/gd/ - Graphic Design&quot; is 4chan's imageboard for graphic design.",
      "is_archived": 1
    },
    {
      "board": "gif",
      "title": "Adult GIF",
      "ws_board": 0,
      "per_page": 15,
      "pages": 10,
      "max_filesize": 4194304,
      "max_webm_filesize": 4194304,
      "max_comment_chars": 2000,
      "max_webm_duration": 300,
      "bump_limit": 300,
      "image_limit": 300,
      "cooldowns": {
        "threads": 600,
        "replies": 60,
        "images": 30
      },
      "meta_description": "&quot;/gif/ - Adult GIF&quot; is 4chan's imageboard dedicated to animated adult GIFs and WEBMs.",
      "is_archived": 1,
      "webm_audio": 1
    },
    {
      "board": "h",
      "title": "Hentai",
      "ws_board": 0,
      "per_page": 15,
      "pages": 10,
      "max_filesize": 4194304,
      "max_webm_filesize": 3145728,
      "max_comment_chars": 2000,
      "max_webm_duration": 120,
      "bump_limit": 300,
      "image_limit": 300,
      "cooldowns": {
        "threads": 600,
        "replies": 60,
        "images": 30
      },
      "meta_description": "&quot;/h/ - Hentai&quot; is 4chan's imageboard for adult Japanese anime hentai images.",
      "is_archived": 1
    },
    {
      "board": "hc",
      "title": "Hardcore",
      "ws_board": 0,
      "per_page": 15,
      "pages": 10,
      "max_filesize": 8388608,
      "max_webm_filesize": 3145728,
      "max_comment_chars": 2000,
      "max_webm_duration": 120,
      "bump_limit": 300,
      "image_limit": 300,
      "cooldowns": {
        "threads": 600,
        "replies": 60,
        "images": 30
      },
      "meta_description": "&quot;/hc/ - Hardcore&quot; is 4chan's imageboard for the posting of adult hardcore pornography.",
      "is_archived": 1,
      "min_image_width": 500,
      "min_image_height": 500
    },
    {
      "board": "his",
      "title": "History & Humanities",
      "ws_board": 1,
      "per_page": 15,
      "pages": 10,
      "max_filesize": 4194304,
      "max_webm_filesize": 3145728,
      "max_comment_chars": 2000,
      "max_webm_duration": 120,
      "bump_limit": 310,
      "image_limit": 150,
      "cooldowns": {
        "threads": 60,
        "replies": 15,
        "images": 15
      },
      "meta_description": "&quot;/his/ - History &amp; Humanities&quot; is 4chan's board for discussing and debating history.",
      "is_archived": 1
    },
    {
      "board": "hm",
      "title": "Handsome Men",
      "ws_board": 0,
      "per_page": 15,
      "pages": 10,
      "max_filesize": 8388608,
      "max_webm_filesize": 3145728,
      "max_comment_chars": 2000,
      "max_webm_duration": 120,
      "bump_limit": 300,
      "image_limit": 150,
      "cooldowns": {
        "threads": 600,
        "replies": 60,
        "images": 30
      },
      "meta_description": "&quot;/hm/ - Handsome Men&quot; is 4chan's imageboard dedicated to sharing adult images of handsome men.",
      "is_archived": 1
    },
    {
      "board": "hr",
      "title": "High Resolution",
      "ws_board": 0,
      "per_page": 15,
      "pages": 10,
      "max_filesize": 8388608,
      "max_webm_filesize": 3145728,
      "max_comment_chars": 2000,
      "max_webm_duration": 120,
      "bump_limit": 300,
      "image_limit": 300,
      "cooldowns": {
        "threads": 600,
        "replies": 60,
        "images": 30
      },
      "meta_description": "&quot;/hr/ - High Resolution&quot; is 4chan's imageboard for the sharing of high resolution images.",
      "is_archived": 1,
      "min_image_width": 1000,
      "min_image_height": 1000
    },
    {
      "board": "i",
      "title": "Oekaki",
      "ws_board": 0,
      "per_page": 15,
      "pages": 10,
      "max_filesize": 4194304,
      "max_webm_filesize": 3145728,
      "max_comment_chars": 2000,
      "max_webm_duration": 120,
      "bump_limit": 300,
      "image_limit": 300,
      "cooldowns": {
        "threads": 600,
        "replies": 60,
        "images": 30
      },
      "meta_description": "&quot;/i/ - Oekaki&quot; is 4chan's oekaki board for drawing and sharing art.",
      "is_archived": 1,
      "oekaki": 1
    },
    {
      "board": "ic",
      "title": "Artwork/Critique",
      "ws_board": 0,
      "per_page": 15,
      "pages": 10,
      "max_filesize": 4194304,
      "max_webm_filesize": 3145728,
      "max_comment_chars": 2000,
      "max_webm_duration": 120,
      "bump_limit": 300,
      "image_limit": 300,
      "cooldowns": {
        "threads": 600,
        "replies": 60,
        "images": 30
      },
      "meta_description": "&quot;/ic/ - Artwork/Critique&quot; is 4chan's imageboard for the discussion and critique of art.",
      "is_archived": 1
    },
    {
      "board": "int",
      "title": "International",
      "ws_board": 1,
      "per_page": 15,
      "pages": 10,
      "max_filesize": 4194304,
      "max_webm_filesize": 3145728,
      "max_comment_chars": 2000,
      "max_webm_duration": 120,
      "bump_limit": 310,
      "image_limit": 150,
      "cooldowns": {
        "threads": 600,
        "replies": 60,
        "images": 60
      },
      "meta_description": "&quot;/int/ - International&quot; is 4chan's international board, for the exchange of foreign language and culture.",
      "is_archived": 1,
      "country_flags": 1
    },
    {
      "board": "jp",
      "title": "Otaku Culture",
      "ws_board": 1,
      "per_page": 15,
      "pages": 10,
      "max_filesize": 4194304,
      "max_webm_filesize": 3145728,
      "max_comment_chars": 5000,
      "max_webm_duration": 120,
      "bump_limit": 310,
      "image_limit": 300,
      "cooldowns": {
        "threads": 3600,
        "replies": 60,
        "images": 60
      },
      "meta_description": "&quot;/jp/ - Otaku Culture&quot; is 4chan's board for discussing Japanese otaku culture.",
      "spoilers": 1,
      "custom_spoilers": 1,
      "is_archived": 1,
      "sjis_tags": 1
    },
    {
      "board": "k",
      "title": "Weapons",
      "ws_board": 1,
      "per_page": 15,
      "pages": 10,
      "max_filesize": 4194304,
      "max_webm_filesize": 3145728,
      "max_comment_chars": 2000,
      "max_webm_duration": 120,
      "bump_limit": 310,
      "image_limit": 150,
      "cooldowns": {
        "threads": 600,
        "replies": 60,
        "images": 60
      },
      "meta_description": "&quot;/k/ - Weapons&quot; is 4chan's imageboard for discussing all types of weaponry, from military tanks to guns and knives.",
      "is_archived": 1
    },
    {
      "board": "lgbt",
      "title": "LGBT",
      "ws_board": 1,
      "per_page": 15,
      "pages": 10,
      "max_filesize": 4194304,
      "max_webm_filesize": 3145728,
      "max_comment_chars": 2000,
      "max_webm_duration": 120,
      "bump_limit": 310,
      "image_limit": 150,
      "cooldowns": {
        "threads": 600,
        "replies": 60,
        "images": 60
      },
      "meta_description": "&quot;/lgbt/ - LGBT&quot; is 4chan's imageboard for Lesbian-Gay-Bisexual-Transgender-Queer and sexuality discussion.",
      "is_archived": 1
    },
    {
      "board": "lit",
      "title": "Literature",
      "ws_board": 1,
      "per_page": 15,
      "pages": 10,
      "max_filesize": 4194304,
      "max_webm_filesize": 3145728,
      "max_comment_chars": 3000,
      "max_webm_duration": 120,
      "bump_limit": 310,
      "image_limit": 150,
      "cooldowns": {
        "threads": 600,
        "replies": 60,
        "images": 60
      },
      "meta_description": "&quot;/lit/ - Literature&quot; is 4chan's board for the discussion of books, authors, and literature.",
      "spoilers": 1,
      "custom_spoilers": 1,
      "is_archived": 1
    },
    {
      "board": "m",
      "title": "Mecha",
      "ws_board": 1,
      "per_page": 15,
      "pages": 10,
      "max_filesize": 4194304,
      "max_webm_filesize": 3145728,
      "max_comment_chars": 2000,
      "max_webm_duration": 120,
      "bump_limit": 310,
      "image_limit": 150,
      "cooldowns": {
        "threads": 600,
        "replies": 60,
        "images": 60
      },
      "meta_description": "&quot;/m/ - Mecha&quot; is 4chan's imageboard for discussing Japanese mecha robots and anime, like Gundam and Macross.",
      "spoilers": 1,
      "custom_spoilers": 4,
      "is_archived": 1
    },
    {
      "board": "mlp",
      "title": "Pony",
      "ws_board": 1,
      "per_page": 15,
      "pages": 10,
      "max_filesize": 4194304,
      "max_webm_filesize": 3145728,
      "max_comment_chars": 2000,
      "max_webm_duration": 120,
      "bump_limit": 500,
      "image_limit": 300,
      "cooldowns": {
        "threads": 600,
        "replies": 60,
        "images": 60
      },
      "meta_description": "&quot;/mlp/ - Pony&quot; is 4chan's imageboard dedicated to the discussion of My Little Pony: Friendship is Magic.",
      "spoilers": 1,
      "custom_spoilers": 1,
      "is_archived": 1
    },
    {
      "board": "mu",
      "title": "Music",
      "ws_board": 1,
      "per_page": 15,
      "pages": 10,
      "max_filesize": 4194304,
      "max_webm_filesize": 3145728,
      "max_comment_chars": 2000,
      "max_webm_duration": 120,
      "bump_limit": 310,
      "image_limit": 150,
      "cooldowns": {
        "threads": 600,
        "replies": 60,
        "images": 60
      },
      "meta_description": "&quot;/mu/ - Music&quot; is 4chan's imageboard for discussing all types of music.",
      "is_archived": 1
    },
    {
      "board": "n",
      "title": "Transportation",
      "ws_board": 1,
      "per_page": 15,
      "pages": 10,
      "max_filesize": 4194304,
      "max_webm_filesize": 3145728,
      "max_comment_chars": 2000,
      "max_webm_duration": 120,
      "bump_limit": 310,
      "image_limit": 150,
      "cooldowns": {
        "threads": 600,
        "replies": 60,
        "images": 60
      },
      "meta_description": "&quot;/n/ - Transportation&quot; is 4chan's imageboard for discussing modes of transportation like trains and bicycles.",
      "is_archived": 1
    },
    {
      "board": "news",
      "title": "Current News",
      "ws_board": 1,
      "per_page": 15,
      "pages": 10,
      "max_filesize": 4194304,
      "max_webm_filesize": 3145728,
      "max_comment_chars": 2000,
      "max_webm_duration": 120,
      "bump_limit": 500,
      "image_limit": 300,
      "cooldowns": {
        "threads": 600,
        "replies": 60,
        "images": 60
      },
      "meta_description": "&quot;/news/ - Current News; is 4chan's board for current news. ",
      "spoilers": 1,
      "custom_spoilers": 1,
      "is_archived": 1,
      "text_only": 1,
      "require_subject": 1
    },
    {
      "board": "o",
      "title": "Auto",
      "ws_board": 1,
      "per_page": 15,
      "pages": 10,
      "max_filesize": 4194304,
      "max_webm_filesize": 3145728,
      "max_comment_chars": 2000,
      "max_webm_duration": 120,
      "bump_limit": 310,
      "image_limit": 150,
      "cooldowns": {
        "threads": 600,
        "replies": 60,
        "images": 60
      },
      "meta_description": "&quot;/o/ - Auto&quot; is 4chan's imageboard for discussing cars and motorcycles.",
      "is_archived": 1
    },
    {
      "board": "out",
      "title": "Outdoors",
      "ws_board": 1,
      "per_page": 15,
      "pages": 10,
      "max_filesize": 5242880,
      "max_webm_filesize": 3145728,
      "max_comment_chars": 2000,
      "max_webm_duration": 120,
      "bump_limit": 310,
      "image_limit": 150,
      "cooldowns": {
        "threads": 600,
        "replies": 60,
        "images": 60
      },
      "meta_description": "&quot;/out/ - Outdoors&quot; is 4chan's imageboard for discussing survivalist skills and outdoor activities such as hiking.",
      "is_archived": 1
    },
    {
      "board": "p",
      "title": "Photography",
      "ws_board": 1,
      "per_page": 15,
      "pages": 10,
      "max_filesize": 5242880,
      "max_webm_filesize": 3145728,
      "max_comment_chars": 2000,
      "max_webm_duration": 120,
      "bump_limit": 310,
      "image_limit": 150,
      "cooldowns": {
        "threads": 600,
        "replies": 60,
        "images": 60
      },
      "meta_description": "&quot;/p/ - Photography&quot; is 4chan's imageboard for sharing and critiquing photos.",
      "is_archived": 1
    },
    {
      "board": "po",
      "title": "Papercraft & Origami",
      "ws_board": 1,
      "per_page": 15,
      "pages": 10,
      "max_filesize": 8388608,
      "max_webm_filesize": 3145728,
      "max_comment_chars": 2000,
      "max_webm_duration": 120,
      "bump_limit": 310,
      "image_limit": 150,
      "cooldowns": {
        "threads": 600,
        "replies": 60,
        "images": 60
      },
      "meta_description": "&quot;/po/ - Papercraft &amp; Origami&quot; is 4chan's imageboard for posting papercraft and origami templates and instructions.",
      "is_archived": 1
    },
    {
      "board": "pol",
      "title": "Politically Incorrect",
      "ws_board": 0,
      "per_page": 20,
      "pages": 10,
      "max_filesize": 4194304,
      "max_webm_filesize": 3145728,
      "max_comment_chars": 2000,
      "max_webm_duration": 120,
      "bump_limit": 300,
      "image_limit": 300,
      "cooldowns": {
        "threads": 90,
        "replies": 30,
        "images": 30
      },
      "meta_description": "&quot;/pol/ - Politically Incorrect&quot; is 4chan's board for discussing and debating politics and current events.",
      "user_ids": 1,
      "is_archived": 1,
      "troll_flags": 1
    },
    {
      "board": "qa",
      "title": "Question & Answer",
      "ws_board": 1,
      "per_page": 15,
      "pages": 10,
      "max_filesize": 4194304,
      "max_webm_filesize": 3145728,
      "max_comment_chars": 2000,
      "max_webm_duration": 120,
      "bump_limit": 310,
      "image_limit": 150,
      "cooldowns": {
        "threads": 600,
        "replies": 60,
        "images": 60
      },
      "meta_description": "&quot;/qa/ - Question &amp; Answer&quot; is 4chan's imageboard for question and answer threads.",
      "is_archived": 1
    },
    {
      "board": "qst",
      "title": "Quests",
      "ws_board": 1,
      "per_page": 15,
      "pages": 10,
      "max_filesize": 8388608,
      "max_webm_filesize": 3145728,
      "max_comment_chars": 3000,
      "max_webm_duration": 120,
      "bump_limit": 750,
      "image_limit": 375,
      "cooldowns": {
        "threads": 600,
        "replies": 60,
        "images": 60
      },
      "meta_description": "&quot;/qst/ - Quests&quot; is 4chan's imageboard for grinding XP.",
      "spoilers": 1,
      "user_ids": 1,
      "is_archived": 1,
      "require_subject": 1,
      "oekaki": 1
    },
    {
      "board": "r",
      "title": "Adult Requests",
      "ws_board": 0,
      "per_page": 15,
      "pages": 10,
      "max_filesize": 8388608,
      "max_webm_filesize": 3145728,
      "max_comment_chars": 2000,
      "max_webm_duration": 120,
      "bump_limit": 300,
      "image_limit": 300,
      "cooldowns": {
        "threads": 600,
        "replies": 60,
        "images": 30
      },
      "meta_description": "&quot;/r/ - Request&quot; is 4chan's imageboard dedicated to fulfilling all types of user requests.",
      "is_archived": 1,
      "webm_audio": 1
    },
    {
      "board": "r9k",
      "title": "ROBOT9001",
      "ws_board": 0,
      "per_page": 15,
      "pages": 10,
      "max_filesize": 2097152,
      "max_webm_filesize": 3145728,
      "max_comment_chars": 2000,
      "max_webm_duration": 120,
      "bump_limit": 500,
      "image_limit": 150,
      "cooldowns": {
        "threads": 600,
        "replies": 60,
        "images": 30
      },
      "meta_description": "&quot;/r9k/ - ROBOT9001&quot; is a board for hanging out and posting greentext stories.",
      "spoilers": 1,
      "is_archived": 1
    },
    {
      "board": "s",
      "title": "Sexy Beautiful Women",
      "ws_board": 0,
      "per_page": 15,
      "pages": 10,
      "max_filesize": 8388608,
      "max_webm_filesize": 3145728,
      "max_comment_chars": 2000,
      "max_webm_duration": 120,
      "bump_limit": 300,
      "image_limit": 150,
      "cooldowns": {
        "threads": 600,
        "replies": 60,
        "images": 30
      },
      "meta_description": "&quot;/s/ - Sexy Beautiful Women&quot; is 4chan's imageboard dedicated to sharing images of softcore pornography.",
      "is_archived": 1,
      "min_image_width": 500,
      "min_image_height": 500
    },
    {
      "board": "s4s",
      "title": "Shit 4chan Says",
      "ws_board": 0,
      "per_page": 15,
      "pages": 10,
      "max_filesize": 2097152,
      "max_webm_filesize": 3145728,
      "max_comment_chars": 2000,
      "max_webm_duration": 120,
      "bump_limit": 300,
      "image_limit": 300,
      "cooldowns": {
        "threads": 300,
        "replies": 60,
        "images": 30
      },
      "meta_description": "&quot;[s4s] - Shit 4chan Says&quot; is 4chan's imageboard for posting dank memes :^)",
      "spoilers": 1,
      "custom_spoilers": 6,
      "is_archived": 1
    },
    {
      "board": "sci",
      "title": "Science & Math",
      "ws_board": 1,
      "per_page": 15,
      "pages": 10,
      "max_filesize": 4194304,
      "max_webm_filesize": 3145728,
      "max_comment_chars": 2000,
      "max_webm_duration": 120,
      "bump_limit": 310,
      "image_limit": 150,
      "cooldowns": {
        "threads": 600,
        "replies": 60,
        "images": 60
      },
      "meta_description": "&quot;/sci/ - Science &amp; Math&quot; is 4chan's board for the discussion of science and math.",
      "is_archived": 1,
      "math_tags": 1
    },
    {
      "board": "soc",
      "title": "Cams & Meetups",
      "ws_board": 0,
      "per_page": 15,
      "pages": 10,
      "max_filesize": 5242880,
      "max_webm_filesize": 3145728,
      "max_comment_chars": 2000,
      "max_webm_duration": 120,
      "bump_limit": 500,
      "image_limit": 300,
      "cooldowns": {
        "threads": 600,
        "replies": 60,
        "images": 30
      },
      "meta_description": "&quot;/soc/ - Cams &amp; Meetups&quot; is 4chan's board for camwhores and meetups.",
      "user_ids": 1,
      "is_archived": 1,
      "forced_anon": 1
    },
    {
      "board": "sp",
      "title": "Sports",
      "ws_board": 1,
      "per_page": 15,
      "pages": 10,
      "max_filesize": 4194304,
      "max_webm_filesize": 3145728,
      "max_comment_chars": 2000,
      "max_webm_duration": 120,
      "bump_limit": 500,
      "image_limit": 300,
      "cooldowns": {
        "threads": 600,
        "replies": 60,
        "images": 60
      },
      "meta_description": "&quot;/sp/ - Sports&quot; is 4chan's imageboard for sports discussion.",
      "is_archived": 1,
      "country_flags": 1
    },
    {
      "board": "t",
      "title": "Torrents",
      "ws_board": 0,
      "per_page": 15,
      "pages": 10,
      "max_filesize": 4194304,
      "max_webm_filesize": 3145728,
      "max_comment_chars": 2000,
      "max_webm_duration": 120,
      "bump_limit": 300,
      "image_limit": 300,
      "cooldowns": {
        "threads": 600,
        "replies": 60,
        "images": 30
      },
      "meta_description": "&quot;/t/ - Torrents&quot; is 4chan's imageboard for posting links and descriptions to torrents.",
      "is_archived": 1
    },
    {
      "board": "tg",
      "title": "Traditional Games",
      "ws_board": 1,
      "per_page": 15,
      "pages": 10,
      "max_filesize": 8388608,
      "max_webm_filesize": 3145728,
      "max_comment_chars": 2000,
      "max_webm_duration": 120,
      "bump_limit": 310,
      "image_limit": 150,
      "cooldowns": {
        "threads": 600,
        "replies": 60,
        "images": 60
      },
      "meta_description": "&quot;/tg/ - Traditional Games&quot; is 4chan's imageboard for discussing traditional gaming, such as board games and tabletop RPGs.",
      "spoilers": 1,
      "custom_spoilers": 2,
      "is_archived": 1
    },
    {
      "board": "toy",
      "title": "Toys",
      "ws_board": 1,
      "per_page": 15,
      "pages": 10,
      "max_filesize": 4194304,
      "max_webm_filesize": 3145728,
      "max_comment_chars": 2000,
      "max_webm_duration": 120,
      "bump_limit": 310,
      "image_limit": 150,
      "cooldowns": {
        "threads": 600,
        "replies": 60,
        "images": 60
      },
      "meta_description": "&quot;/toy/ - Toys&quot; is 4chan's imageboard for talking about all kinds of toys!",
      "is_archived": 1
    },
    {
      "board": "trash",
      "title": "Off-Topic",
      "ws_board": 0,
      "per_page": 15,
      "pages": 10,
      "max_filesize": 4194304,
      "max_webm_filesize": 3145728,
      "max_comment_chars": 2000,
      "max_webm_duration": 120,
      "bump_limit": 300,
      "image_limit": 300,
      "cooldowns": {
        "threads": 600,
        "replies": 60,
        "images": 30
      },
      "meta_description": "&quot;/trash/ - Off-topic&quot; is 4chan's imageboard jail for off-topic threads.",
      "forced_anon": 1
    },
    {
      "board": "trv",
      "title": "Travel",
      "ws_board": 1,
      "per_page": 15,
      "pages": 10,
      "max_filesize": 8388608,
      "max_webm_filesize": 3145728,
      "max_comment_chars": 2000,
      "max_webm_duration": 120,
      "bump_limit": 310,
      "image_limit": 150,
      "cooldowns": {
        "threads": 600,
        "replies": 60,
        "images": 60
      },
      "meta_description": "&quot;/trv/ - Travel&quot; is 4chan's imageboard dedicated to travel and the countries of the world.",
      "is_archived": 1
    },
    {
      "board": "tv",
      "title": "Television & Film",
      "ws_board": 1,
      "per_page": 15,
      "pages": 10,
      "max_filesize": 4194304,
      "max_webm_filesize": 3145728,
      "max_comment_chars": 2000,
      "max_webm_duration": 120,
      "bump_limit": 310,
      "image_limit": 150,
      "cooldowns": {
        "threads": 600,
        "replies": 60,
        "images": 60
      },
      "meta_description": "&quot;/tv/ - Television &amp; Film&quot; is 4chan's imageboard dedicated to the discussion of television and film.",
      "spoilers": 1,
      "custom_spoilers": 5,
      "is_archived": 1
    },
    {
      "board": "u",
      "title": "Yuri",
      "ws_board": 0,
      "per_page": 15,
      "pages": 10,
      "max_filesize": 4194304,
      "max_webm_filesize": 3145728,
      "max_comment_chars": 2000,
      "max_webm_duration": 120,
      "bump_limit": 300,
      "image_limit": 300,
      "cooldowns": {
        "threads": 600,
        "replies": 60,
        "images": 30
      },
      "meta_description": "&quot;/u/ - Yuri&quot; is 4chan's imageboard for yuri hentai images.",
      "spoilers": 1,
      "is_archived": 1
    },
    {
      "board": "v",
      "title": "Video Games",
      "ws_board": 1,
      "per_page": 20,
      "pages": 10,
      "max_filesize": 4194304,
      "max_webm_filesize": 3145728,
      "max_comment_chars": 2000,
      "max_webm_duration": 120,
      "bump_limit": 500,
      "image_limit": 300,
      "cooldowns": {
        "threads": 600,
        "replies": 60,
        "images": 60
      },
      "meta_description": "&quot;/v/ - Video Games&quot; is 4chan's imageboard dedicated to the discussion of PC and console video games.",
      "spoilers": 1,
      "custom_spoilers": 1,
      "is_archived": 1
    },
    {
      "board": "vg",
      "title": "Video Game Generals",
      "ws_board": 1,
      "per_page": 15,
      "pages": 10,
      "max_filesize": 4194304,
      "max_webm_filesize": 3145728,
      "max_comment_chars": 2000,
      "max_webm_duration": 120,
      "bump_limit": 750,
      "image_limit": 375,
      "cooldowns": {
        "threads": 600,
        "replies": 90,
        "images": 120
      },
      "meta_description": "&quot;/vg/ - Video Game Generals&quot; is 4chan's imageboard dedicated to the discussion of PC and console video games.",
      "spoilers": 1,
      "custom_spoilers": 1,
      "is_archived": 1,
      "require_subject": 1
    },
    {
      "board": "vip",
      "title": "Very Important Posts",
      "ws_board": 1,
      "per_page": 15,
      "pages": 10,
      "max_filesize": 4194304,
      "max_webm_filesize": 3145728,
      "max_comment_chars": 2000,
      "max_webm_duration": 120,
      "bump_limit": 300,
      "image_limit": 300,
      "cooldowns": {
        "threads": 600,
        "replies": 60,
        "images": 60
      },
      "meta_description": "&quot;/vip/ - Very Important Posts&quot; is 4chan's imageboard for Pass users.",
      "spoilers": 1,
      "is_archived": 1,
      "sjis_tags": 1,
      "oekaki": 1
    },
    {
      "board": "vp",
      "title": "Pokémon",
      "ws_board": 1,
      "per_page": 15,
      "pages": 10,
      "max_filesize": 4194304,
      "max_webm_filesize": 3145728,
      "max_comment_chars": 2000,
      "max_webm_duration": 120,
      "bump_limit": 310,
      "image_limit": 150,
      "cooldowns": {
        "threads": 600,
        "replies": 60,
        "images": 60
      },
      "meta_description": "&quot;/vp/ - Pok&eacute;mon&quot; is 4chan's imageboard dedicated to discussing the Pok&eacute;mon series of video games and shows.",
      "spoilers": 1,
      "custom_spoilers": 1,
      "is_archived": 1
    },
    {
      "board": "vr",
      "title": "Retro Games",
      "ws_board": 1,
      "per_page": 15,
      "pages": 10,
      "max_filesize": 4194304,
      "max_webm_filesize": 3145728,
      "max_comment_chars": 2000,
      "max_webm_duration": 120,
      "bump_limit": 500,
      "image_limit": 300,
      "cooldowns": {
        "threads": 600,
        "replies": 60,
        "images": 60
      },
      "meta_description": "&quot;/vr/ - Retro Games&quot; is 4chan's imageboard for discussing retro console video games and classic arcade games.",
      "spoilers": 1,
      "custom_spoilers": 2,
      "is_archived": 1
    },
    {
      "board": "w",
      "title": "Anime/Wallpapers",
      "ws_board": 1,
      "per_page": 15,
      "pages": 10,
      "max_filesize": 6291456,
      "max_webm_filesize": 3145728,
      "max_comment_chars": 2000,
      "max_webm_duration": 120,
      "bump_limit": 310,
      "image_limit": 300,
      "cooldowns": {
        "threads": 600,
        "replies": 60,
        "images": 60
      },
      "meta_description": "&quot;/w/ - Anime/Wallpapers&quot; is 4chan's imageboard for posting Japanese anime wallpapers.",
      "is_archived": 1,
      "min_image_width": 480,
      "min_image_height": 600
    },
    {
      "board": "wg",
      "title": "Wallpapers/General",
      "ws_board": 0,
      "per_page": 15,
      "pages": 10,
      "max_filesize": 6291456,
      "max_webm_filesize": 3145728,
      "max_comment_chars": 2000,
      "max_webm_duration": 120,
      "bump_limit": 300,
      "image_limit": 300,
      "cooldowns": {
        "threads": 600,
        "replies": 60,
        "images": 30
      },
      "meta_description": "&quot;/wg/ - Wallpapers/General&quot; is 4chan's imageboard for posting general wallpapers.",
      "is_archived": 1,
      "min_image_width": 480,
      "min_image_height": 600
    },
    {
      "board": "wsg",
      "title": "Worksafe GIF",
      "ws_board": 1,
      "per_page": 15,
      "pages": 10,
      "max_filesize": 6291456,
      "max_webm_filesize": 6291456,
      "max_comment_chars": 2000,
      "max_webm_duration": 300,
      "bump_limit": 310,
      "image_limit": 150,
      "cooldowns": {
        "threads": 600,
        "replies": 60,
        "images": 60
      },
      "meta_description": "&quot;/wsg/ - Worksafe GIF&quot; is 4chan's imageboard dedicated to sharing worksafe animated GIFs and WEBMs.",
      "is_archived": 1,
      "webm_audio": 1
    },
    {
      "board": "wsr",
      "title": "Worksafe Requests",
      "ws_board": 1,
      "per_page": 15,
      "pages": 10,
      "max_filesize": 8388608,
      "max_webm_filesize": 3145728,
      "max_comment_chars": 2000,
      "max_webm_duration": 120,
      "bump_limit": 310,
      "image_limit": 150,
      "cooldowns": {
        "threads": 600,
        "replies": 60,
        "images": 60
      },
      "meta_description": "&quot;/wsr/ - Worksafe Requests&quot; is 4chan's imageboard dedicated to fulfilling non-NSFW requests.",
      "is_archived": 1,
      "webm_audio": 1
    },
    {
      "board": "x",
      "title": "Paranormal",
      "ws_board": 1,
      "per_page": 15,
      "pages": 10,
      "max_filesize": 4194304,
      "max_webm_filesize": 3145728,
      "max_comment_chars": 2000,
      "max_webm_duration": 120,
      "bump_limit": 310,
      "image_limit": 150,
      "cooldowns": {
        "threads": 600,
        "replies": 60,
        "images": 60
      },
      "meta_description": "&quot;/x/ - Paranormal&quot; is 4chan's imageboard for the discussion of paranormal, spooky pictures and conspiracy theories.",
      "is_archived": 1
    },
    {
      "board": "y",
      "title": "Yaoi",
      "ws_board": 0,
      "per_page": 15,
      "pages": 10,
      "max_filesize": 4194304,
      "max_webm_filesize": 3145728,
      "max_comment_chars": 2000,
      "max_webm_duration": 120,
      "bump_limit": 300,
      "image_limit": 300,
      "cooldowns": {
        "threads": 600,
        "replies": 60,
        "images": 30
      },
      "meta_description": "&quot;/y/ - Yaoi&quot; is 4chan's imageboard for posting adult yaoi hentai images.",
      "is_archived": 1
    }
  ],
  "troll_flags": {
    "AC": "Anarcho-Capitalist",
    "AN": "Anarchist",
    "BL": "Black Nationalist",
    "CF": "Confederate",
    "CM": "Communist",
    "CT": "Catalonia",
    "DM": "Democrat",
    "EU": "European",
    "FC": "Fascist",
    "GN": "Gadsden",
    "GY": "Gay",
    "JH": "Jihadi",
    "KN": "Kekistani",
    "MF": "Muslim",
    "NB": "National Bolshevik",
    "NZ": "Nazi",
    "PC": "Hippie",
    "PR": "Pirate",
    "RE": "Republican",
    "TM": "Templar",
    "TR": "Tree Hugger",
    "UN": "United Nations",
    "WP": "White Supremacist"
  }
}
```



Parameter       | Type       | Description
----------------|------------|-------------
board           | string     | 4chan board.
title           | string     | 4chan board title.
description     | string     | 4chan board description.




## 4chanThreadViewer

> Sample Data

```cli
{
  "board": "biz",
  "thread_number": "904256"
}
```
4chan thread from a specified board.


### Request Parameters

> Sample Request

```shell
curl -H "Accept: application/json" -H "Content-Type: application/json" -d '["biz","904256"]' https://api.maplenodes.com/xrs/4chanThreadViewer
```

<code class="api-call">4chanThreadViewer [board] [thread_number]</code>

Parameter       | Type       | Description
----------------|------------|-------------
board           | string     | 4chan board.
thread_number   | int        | Thread number to view.


### Response Parameters

<aside class="success">
200 OK
</aside>

> Sample 200 Response

```shell
[
  {
    "subject": "Welcome to /biz/ - Business &amp; Finance",
    "total_replies": 0,
    "total_images": 0
  },
  {
    "name": "Anonymous",
    "id": "Mod",
    "time": "09/24/15(Thu)13:11:36",
    "post_number": 904256,
    "reply_to": 0,
    "comment": "This board is for the discussion of topics related to business, economics, financial markets, securities, currencies (including cryptocurrencies), commodities, etc -- as well as topics relating to starting and running a business.<br><br>Discussions of government policy must be strictly limited to economic policies (fiscal and monetary). Discussions of a political nature should be posted on <a href=\"/pol/\" class=\"quotelink\">&gt;&gt;&gt;/pol/</a>. Global Rule 3 is also obviously in effect.<br><br>Note: /biz/ is NOT a place for ADVERTISING or SOLICITING. Do NOT use it to promote your business, ventures, or anything you may have an interest in. Anything that looks remotely like advertising or soliciting will be removed. Begging/asking (including tipping) for cyptocurrencies or asking for money/capital is also strictly forbidden. Want to advertise? Buy a banner /biz/ targeted banner ad: <a href=\"https://www.4chan.org/advertise?selfserve\" target=\"_blank\">https://www.4chan.org/advertise?sel<wbr>fserve</a>"
  }
]
```


Parameter       | Type       | Description
----------------|------------|-------------
subject         | string     | Thread subject title.
total_replies   | int        | Number of total replies.
total_images    | int        | Number of total images.
name            | string     | Username of poster.
id              | string     | 4chan user ID.
time            | string     | Timestamp of posted message.
post_number     | string     | Post number.
reply_to        | string     | Reply to post number.
comment         | string     | Comment from user.





## 4chanThreadViewerPrice

> Sample Data

```cli
{
  "board": "biz",
  "thread_number": "904256",
  "ticker": "BTC",
  "currency": "USD"
}
```
4chan thread from a specified board with pricing information of a specified crypto ticker based off the original post creation time.


### Request Parameters

> Sample Request

```shell
curl -H "Accept: application/json" -H "Content-Type: application/json" -d '["biz","904256","BTC","USD"]' https://api.maplenodes.com/xrs/4chanThreadViewerPrice
```

<code class="api-call">4chanThreadViewerPrice [board] [thread_number] [ticker] [currency]</code>

Parameter       | Type       | Description
----------------|------------|-------------
board           | string     | 4chan board.
thread_number   | int        | Thread number to view.
ticker          | string     | Crypto asset ticker.
currency        | string     | World currency.


### Response Parameters

<aside class="success">
200 OK
</aside>

> Sample 200 Response

```shell
[
  {
    "BTC": {
      "USD": 233.76000000
    }
  },
  {
    "percent_change_24h": "-0.85"
  },
  {
    "subject": "Welcome to /biz/ - Business &amp; Finance",
    "total_replies": 0,
    "total_images": 0
  },
  {
    "name": "Anonymous",
    "id": "Mod",
    "time": "09/24/15(Thu)13:11:36",
    "post_number": 904256,
    "reply_to": 0,
    "comment": "This board is for the discussion of topics related to business, economics, financial markets, securities, currencies (including cryptocurrencies), commodities, etc -- as well as topics relating to starting and running a business.<br><br>Discussions of government policy must be strictly limited to economic policies (fiscal and monetary). Discussions of a political nature should be posted on <a href=\"/pol/\" class=\"quotelink\">&gt;&gt;&gt;/pol/</a>. Global Rule 3 is also obviously in effect.<br><br>Note: /biz/ is NOT a place for ADVERTISING or SOLICITING. Do NOT use it to promote your business, ventures, or anything you may have an interest in. Anything that looks remotely like advertising or soliciting will be removed. Begging/asking (including tipping) for cyptocurrencies or asking for money/capital is also strictly forbidden. Want to advertise? Buy a banner /biz/ targeted banner ad: <a href=\"https://www.4chan.org/advertise?selfserve\" target=\"_blank\">https://www.4chan.org/advertise?sel<wbr>fserve</a>"
  }
]
```

Parameter          | Type       | Description
-------------------|------------|-------------
ticker             | string     | Price of crypto ticker in world currency of thread timestamp.
percent_change_24h | int        | Percent change.
subject            | string     | Thread subject title.
total_replies      | int        | Number of total replies.
total_images       | int        | Number of total images.
name               | string     | Username of poster.
id                 | string     | 4chan user ID.
time               | string     | Timestamp of posted message.
post_number        | string     | Post number.
reply_to           | string     | Reply to post number.
comment            | string     | Comment from user.





## 4chanThreads

> Sample Data

```cli
{
  "board": "biz"
}
```
4chan threads from a specified board.


### Request Parameters

> Sample Request

```shell
curl -H "Accept: application/json" -H "Content-Type: application/json" -d '["biz"]' https://api.maplenodes.com/xrs/4chanThreads
```

<code class="api-call">4chanThreads [board]</code>

Parameter       | Type       | Description
----------------|------------|-------------
board           | string     | 4chan board.


### Response Parameters

<aside class="success">
200 OK
</aside>

> Sample 200 Response

```shell
[
  {
    "number": 904256,
    "time": "09/24/15(Thu)13:11:36",
    "subject": "Welcome to /biz/ - Business &amp; Finance",
    "original_post": "This board is for the discussion of topics related to business, economics, financial markets, securities, currencies (including cryptocurrencies), commodities, etc -- as well as topics relating to starting and running a business.<br><br>Discussions of government policy must be strictly limited to economic policies (fiscal and monetary). Discussions of a political nature should be posted on <a href=\"/pol/\" class=\"quotelink\">&gt;&gt;&gt;/pol/</a>. Global Rule 3 is also obviously in effect.<br><br>Note: /biz/ is NOT a place for ADVERTISING or SOLICITING. Do NOT use it to promote your business, ventures, or anything you may have an interest in. Anything that looks remotely like advertising or soliciting will be removed. Begging/asking (including tipping) for cyptocurrencies or asking for money/capital is also strictly forbidden. Want to advertise? Buy a banner /biz/ targeted banner ad: <a href=\"https://www.4chan.org/advertise?selfserve\" target=\"_blank\">https://www.4chan.org/advertise?sel<wbr>fserve</a>",
    "replies": 0,
    "images": 0
  },
  {
    "number": 4884770,
    "time": "12/08/17(Fri)08:35:13",
    "subject": "NO BEGGING",
    "original_post": "<span style=\"font-weight:600;font-size:150%;line-height:1.5;\">Begging or asking for &#039;free money&#039;/crypto is strictly forbidden. Encouraging beggars, or posting any kind of &#039;free money&#039; offer is also strictly forbidden.</span>",
    "replies": 0,
    "images": 0
  },
  {
    "number": 18891582,
    "time": "05/05/20(Tue)17:33:14",
    "subject": "/smg/ - Stock Market General",
    "original_post": "the abyss edition<br><br><span class=\"quote\">&gt;Brokers</span><br>https://pastebin.com/F1yujtVq<br><br><span class=\"quote\">&gt;Stock market Words</span><br>https://pastebin.com/VtnpN5iJ<br><br><span class=\"quote\">&gt;Risk Management</span><br>https://pastebin.com/sqJUcbjp<br><br><span class=\"quote\">&gt;Live Bloomberg Stream</span><br>http://www.livenewson.com/american/<wbr>bloomberg-television-business.html<br><br><span class=\"quote\">&gt;Educational Sites</span><br>https://www.investopedia.com/<br>https://www.khanacademy.org/economi<wbr>cs-finance-domain<br>https://nhentai.net/tag/crossdressi<wbr>ng/<br><br><span class=\"quote\">&gt;Free Charts</span><br>http://www.tradingview.com<br>https://www.finscreener.com/<br><br><span class=\"quote\">&gt;Screeners</span><br>https://finviz.com/<br>https://www.tradingview.com/screene<wbr>r<br>https://etfdb.com/<br><br><span class=\"quote\">&gt;Pre-Market Data and Live Data</span><br>https://www.investing.com/indices/i<wbr>ndices-futures<br>https://finance.yahoo.com/<br><br><span class=\"quote\">&gt;Bio-pharma Catalyst Calendar</span><br>https://biopharmcatalyst.com<br><br><span class=\"quote\">&gt;Boomer Investing 101</span><br>https://www.bogleheads.org/wiki/Get<wbr>ting_started<br><br><span class=\"quote\">&gt;Dividend Reinvestment (DRIP) Calculator</span><br>https://www.dividendchannel.com/dri<wbr>p-returns-calculator/<br><br><span class=\"quote\">&gt;List of hedge fund holdings</span><br>https://fintel.io/<br><br><span class=\"quote\">&gt;Misc</span><br>https://squeezemetrics.com/monitor<br>https://market24hclock.com/<br><br><a href=\"/biz/thread/18889964#p18889964\" class=\"quotelink\">&gt;&gt;18889964</a>",
    "replies": 184,
    "images": 35
  },
  {
    "number": 18894337,
    "time": "05/05/20(Tue)20:05:15",
    "subject": "I love you so much biz",
    "original_post": "I love you all anons, you boiz mean a lot to me, and even tho sometimes we can be fighting over what coins to buy, I still love you afterwards all the same &lt;3 &lt;3 &lt;3",
    "replies": 4,
    "images": 0
  },
  {
    "number": 18895321,
    "time": "05/05/20(Tue)21:08:11",
    "subject": "I’m about to drop 10k on HEX, be nice to me frens",
    "original_post": "But only if someone expains me how can I cash out. IQ 40 brainlet here",
    "replies": 0,
    "images": 0
  },
  {
    "number": 18894264,
    "time": "05/05/20(Tue)20:00:02",
    "subject": "Any Suggestions",
    "original_post": "Best way/resources to learn technical analysis and fundamental analysis?",
    "replies": 4,
    "images": 1
  },
  {
    "number": 18894019,
    "time": "05/05/20(Tue)19:44:20",
    "subject": null,
    "original_post": "<span class=\"quote\">&gt;Janny are you okay?</span><br>Janny are you okay?<br><br><span class=\"quote\">&gt;Are you okay, Janny?</span>",
    "replies": 14,
    "images": 5
  },
  {
    "number": 18894702,
    "time": "05/05/20(Tue)20:26:48",
    "subject": "do I need to say anything? you just win",
    "original_post": "all time high go brrrrrrrrrr<br>and this... is... to go... even further... AND BEYOOOOOOOND!",
    "replies": 5,
    "images": 0
  },
  {
    "number": 18895317,
    "time": "05/05/20(Tue)21:08:01",
    "subject": null,
    "original_post": "Is this true? Should I look into BSV more? I like Money Button and Twetch but don&#039;t know anything else",
    "replies": 0,
    "images": 0
  },
  {
    "number": 18895316,
    "time": "05/05/20(Tue)21:07:58",
    "subject": null,
    "original_post": "tha tha thats bullish",
    "replies": 0,
    "images": 0
  },
  {
    "number": 18895305,
    "time": "05/05/20(Tue)21:07:22",
    "subject": null,
    "original_post": "The only way to cure the incel problem is to reduce the demand of women and increase the supply of women. It&#039;s basic economics.<br>We need to start turning men into women with hrt. Starting with the failed males on this board<br><br>Join our server and turn yourself into a cute girl: discord gg ZEasuV",
    "replies": 1,
    "images": 0
  },
  {
    "number": 18895246,
    "time": "05/05/20(Tue)21:02:57",
    "subject": "Elimination of Payroll and Capital Gains Taxes",
    "original_post": "Sorry commies, your time is up.",
    "replies": 7,
    "images": 0
  },
  {
    "number": 18895285,
    "time": "05/05/20(Tue)21:05:21",
    "subject": "Bulls and Bears....GET IN HERE",
    "original_post": "Let&#039;s have a civilized discussion here...<br>why are you the way that you are right now? What&#039;s your outlook on the economy?",
    "replies": 1,
    "images": 0
  },
  {
    "number": 18894986,
    "time": "05/05/20(Tue)20:44:28",
    "subject": null,
    "original_post": "Why&#039;s the price of Nintendo Switch so high right now despite being released in 2017?<br>Is it defying Moore&#039;s law?",
    "replies": 14,
    "images": 1
  },
  {
    "number": 18894694,
    "time": "05/05/20(Tue)20:26:23",
    "subject": "YOUTUBE SCAM",
    "original_post": "Right now there is a live event going on on YouTube under the account name “Ledger CEO” where they are saying they are basically doubling your bitcoin; if you send them some they will send back double and a bonus on top (the runescape classic) along with a prerecorded video interview playing in the corner of the screen, when you click on the account it’s clearly someone from india and all the rest of the videos have under 1000 views about miscellaneous topics. Somehow YouTube has let this get high in the trending and when I was there there was over 20,000 people watching. Spread the word sirs, don’t lose your bitcoin to pajeets",
    "replies": 3,
    "images": 2
  },
  {
    "number": 18894963,
    "time": "05/05/20(Tue)20:42:59",
    "subject": null,
    "original_post": "What are you besides /biz/? Financial stability is one of the four pillars of happiness, but what other boards/hobbies do you have? For me, I&#039;m /biz/, /ck/, /fit/, /pol/.",
    "replies": 12,
    "images": 3
  },
  {
    "number": 18892195,
    "time": "05/05/20(Tue)18:01:16",
    "subject": "500k dumps by Chainlink",
    "original_post": "The 700k dumps started two weeks after they pumped their price with a Google &quot;partnership&quot; in July 2019. Now they started 500k dumps in a different address. Is the top in again?",
    "replies": 62,
    "images": 13
  },
  {
    "number": 18887666,
    "time": "05/05/20(Tue)14:50:52",
    "subject": "Chainlink insider back, any questions?",
    "original_post": "<a href=\"/biz/thread/18793514#p18793514\" class=\"quotelink\">&gt;&gt;18793514</a><br><br>Sats continue to dump, insider back for a few. By now you&#039;re probably aware of Gemini. Even then, volume is much lower because bots are off.<br><br>https://coinmarketcap.com/currencie<wbr>s/chainlink/<br><br>Volume is 1/3 what it was recently. It was a large reason for price spikes given some of the arbitrage and wash trading happening behind the scenes. CZ is a bad actor, all I&#039;ll say about him. If you know our history, you&#039;ll know they listed our token without contacting us. <br><br>That said, exchange listings are responsible for the majority of the gains, insiders know ahead of time and buy more supply, this latest episode was the Winklevoss&#039; twins doing. What&#039;s frustrating is it&#039;s inorganic, and the price isn&#039;t reflective of network usage or legitimate enterprise adoption. We have been silent on that front for good (or bad) reason, it&#039;s hard to convince the older generations that the concept is as important as it is to future regulatory actions and adoption. <br><br>Ask away, I have 20 minutes",
    "replies": 106,
    "images": 12
  },
  {
    "number": 18895302,
    "time": "05/05/20(Tue)21:07:04",
    "subject": "T minutes 58 minutes",
    "original_post": "I can&#039;t believe it&#039;s really happening. After years of memes and fudding and hoping and hodling and pajeet scammers and P&amp;D meme tokens. The day is finally fucking here.<br><br>Remember this moment. Because in 57 minutes we&#039;ll all be on the other side. We fucking did it and it&#039;s every bit as beautiful as I had hoped. Thank you. THANK YOU.",
    "replies": 0,
    "images": 0
  },
  {
    "number": 18895300,
    "time": "05/05/20(Tue)21:06:58",
    "subject": null,
    "original_post": "Why is the hash rate so high",
    "replies": 0,
    "images": 0
  },
  {
    "number": 18887763,
    "time": "05/05/20(Tue)14:54:15",
    "subject": "DAILY 32 ETHEREUM CHECK!",
    "original_post": "For the love of god, don&#039;t miss out on staking /biz/",
    "replies": 39,
    "images": 3
  },
  {
    "number": 18893440,
    "time": "05/05/20(Tue)19:12:09",
    "subject": null,
    "original_post": "If TA can’t predict future events, why are people still using it?",
    "replies": 24,
    "images": 3
  },
  {
    "number": 18894569,
    "time": "05/05/20(Tue)20:18:36",
    "subject": "Petition to ban HEX threads",
    "original_post": "We are now at an impasse that must be resolved.<br>The state of this board has been really deteriorating and hemorrhaging users because of this nonstop shilling of this shitcoin. <br>If mods don&#039;t make a decision, this board will die a slow and painful die.<br><br>Due to the fact that HEX has been proven to be a legitimate scam with quantifiable evidence; I suggest we make an exception to &quot;free speech&quot; rules and make it a 3 day ban for posting about HEX.<br>HEX is the only &quot;&quot;&quot;stock&quot;&quot;&quot; that has been proven without a doubt that it is a scam hence why it was banned from whale alert. <br><br>We need to follow suit and bring this board to a more bearable state. <br><br>Vote<br><br>https://www.strawpoll.me/19958774",
    "replies": 32,
    "images": 4
  },
  {
    "number": 18894502,
    "time": "05/05/20(Tue)20:15:32",
    "subject": "Next crypto bullrun",
    "original_post": "Hate it all you want, but this thing will cause the next crypto bullrun because of the million copy cats this will create. A rising tide raises all boats.",
    "replies": 13,
    "images": 2
  },
  {
    "number": 18895294,
    "time": "05/05/20(Tue)21:06:12",
    "subject": "BUY STARBUCKS",
    "original_post": "JC says so. All small coffee shops are getting fucked from COVID-19",
    "replies": 0,
    "images": 0
  },
  {
    "number": 18893779,
    "time": "05/05/20(Tue)19:30:50",
    "subject": null,
    "original_post": "What&#039;s the single most expensive item in your house? For me, it&#039;s my gaming PC.",
    "replies": 51,
    "images": 3
  },
  {
    "number": 18892507,
    "time": "05/05/20(Tue)18:18:15",
    "subject": "JULY IS THE BOTTOM",
    "original_post": "It will take atleast a few weeks to a month before burgers realize they fucked up relaxing the lockdowns too early.<br><br>JULY IS THE BOTTOM. <br><br>S&amp;P 500 target: $1900<br>Gold target: $1300<br>Bitcoin target: $3300<br><br>After this, the stock market will take at least 2 years to recover BUT expect gold and bitcoin to go through the fucking moon end of this year.<br><br>Oh and screencap this and post back on /biz/ in a few months time to prove how you missed another big chance to make it.",
    "replies": 7,
    "images": 3
  },
  {
    "number": 18895110,
    "time": "05/05/20(Tue)20:52:39",
    "subject": null,
    "original_post": "Chainlink&#039;s model will not succeed, here is why. The cost/risk of attacking the oracle nodes must always exceed that of the exploitable value of the contracts that rely on them. Thus, either smart contracts will never handle large amounts of value, or the oracle network must be exceedingly large and expensive to attack. It doesn&#039;t make sense for it to be more expensive to secure a price feed than the actual underlying contracts that rely on it. By relying on the oracle nodes, you&#039;ve made it easier to attack. Security of the real world price feeds themselves is irrelevant as oracle nodes are now the source of truth. Doesn&#039;t matter how secure coinbase is, for example, if you&#039;re not getting your data directly from it.<br><br>So... what if real world feeds signed their data? Then the oracle nodes could just pass it on and you can verify the data is untampered, right? Yes, exactly, so why are oracles needed for consensus on signed data? They&#039;re just glorified https clients at that point. They are unnecessary.<br><br>I see the only real solution being that there is a standardized data/view spec contract much like the erc20-721 contract. Data providers like Coinbase publish data directly on chain. It is verifiable because the contract is written in a way where only the creator of the contract can add new data points, and to do so implies control of the private key of the owner. Aggregation of multiple data contracts into a single combined one using median or some other filtering function makes it so that at least 50% of the data contracts must be compromised in order for the attack to be successful. For data contracts to be compromised, either the network must be compromised, or the data provider themselves must be compromised. Assuming network is not compromised, as we have bigger issues if that happens, that means 50% of the data providers must be attacked. If 50% of the large exchanges are simultaneous compromised, i think it&#039;s fine if everything goes to shit",
    "replies": 4,
    "images": 1
  },
  {
    "number": 18889554,
    "time": "05/05/20(Tue)15:59:21",
    "subject": "LCX listing in HitBTC next weeeeeeek!!!!",
    "original_post": "LCX is heading by far the vote for the next token to be listed in HitBTC...<br>COUNTDOWN TIME 5 DAYS<br>Get on board foools!!!",
    "replies": 13,
    "images": 3
  },
  {
    "number": 18890959,
    "time": "05/05/20(Tue)17:03:14",
    "subject": "Getting Chainlink vibes",
    "original_post": "The team has been building for years w/ no marketing<br>The team works with many eth developers and Vitalik tweeted about their project. <br>Consensys Backed, yet still under the radar. <br>Profit model built in to the network, dont have to dump tokens.<br>Super small market cap. <br>They plan to market at main net (august most likely) just like link did last may (look at what happened to link price) <br>Can be built into the backend of any wallet, exchange, staking service<br>Accumulation going on.<br>Only place being shilled is by high IQ biz<br>acap&#039;s proven success record of finding gems<br>The community is growing exponentially (check discord, many joins each day)<br>Less than 2,000 wallets holding rpl (what happens when it gets to 5k, 10k, or 100k like link?)<br>I could keep going on but maybe you get the point. I didn&#039;t think another link-like gem would come along ever, but I was wrong.",
    "replies": 37,
    "images": 7
  },
  {
    "number": 18892423,
    "time": "05/05/20(Tue)18:13:33",
    "subject": null,
    "original_post": "What did /biz/ talk about before cryptos?",
    "replies": 49,
    "images": 5
  },
  {
    "number": 18880755,
    "time": "05/05/20(Tue)09:39:12",
    "subject": null,
    "original_post": "Post /biz/ dream pads",
    "replies": 278,
    "images": 91
  },
  {
    "number": 18894426,
    "time": "05/05/20(Tue)20:11:09",
    "subject": "Please understand, this is all I can reveal at the current time.",
    "original_post": "George--<br><br>It was a pleasure seeing you at Brdo Castle. Thank you again for your kind words and commitments. I look forward to visiting Prairie Chapel Ranch and meeting your wonderful family.<br><br>I write to inform you of the status of &#039;Rusalka&#039;. Please know that our nation&#039;s work on this project was the crown jewel of Soviet science, more important than the space program and nuclear program combined. Indeed, it has the potential to shape the course of human history for centuries to come.<br><br>For this reason, we cannot at this time reveal to you, our friends in the US, the location of the lighthouse, and we absolutely cannot commit to any request for dismantling or demolishing it.<br><br>Please understand, and know that this determination has no impact on our other commitments made to the US and the NATO alliance. We seek to move forward to a more prosperous future as close allies and trading partners.<br><br>--Vladimir.",
    "replies": 60,
    "images": 3
  },
  {
    "number": 18894416,
    "time": "05/05/20(Tue)20:10:19",
    "subject": null,
    "original_post": "My employer is trying to force us to come back to work with masks on. I told them I refuse to wear a mask cause its hard to breathe and i have a history of athsma.<br><br>Can they force me to wear a mask? Can I sue or take any other action if they fire me for refusing to wear one?",
    "replies": 3,
    "images": 1
  },
  {
    "number": 18894880,
    "time": "05/05/20(Tue)20:37:45",
    "subject": "TETHER ONLY HOLD 241 MILLION!!!!!",
    "original_post": "<span class=\"quote\">&gt;Tether minted over $1.2 billion in USDT tokens in April.</span><br><span class=\"quote\">&gt;$67 million left the USDT treasury in the last 24 hours.</span><br><span class=\"quote\">&gt;Only $241 million in USDT tokens remain in the Tether Treasury.</span><br><br>Stablecoin platform Tether has drawn up controversy in the crypto community due to its lack of transparency. The platform minted over a $1.2 billion in USDT tokens last month, without providing external audit data proving the platform holds $8B in liquidatable assets.",
    "replies": 6,
    "images": 1
  },
  {
    "number": 18892041,
    "time": "05/05/20(Tue)17:53:52",
    "subject": null,
    "original_post": "There are no affordable suburbs left in America that aren&#039;t overrun with niggers or spics. If you&#039;re white but not rich, there&#039;s no place for you anymore. Most of us will die never having attained the standard of living that our parents and grandparents had.",
    "replies": 96,
    "images": 8
  },
  {
    "number": 18893395,
    "time": "05/05/20(Tue)19:09:41",
    "subject": null,
    "original_post": "What does he hold?",
    "replies": 14,
    "images": 0
  },
  {
    "number": 18895258,
    "time": "05/05/20(Tue)21:03:41",
    "subject": null,
    "original_post": "Is it worth it to stake?",
    "replies": 0,
    "images": 0
  },
  {
    "number": 18894450,
    "time": "05/05/20(Tue)20:12:43",
    "subject": "Orchid (OXT) VPN token pushed by Coinbase",
    "original_post": "What does /biz/ think about this one? Just a pump and dump or is the multi hopping theory behind it actually valid, ushering in a new age of decentralized VPN?",
    "replies": 9,
    "images": 1
  },
  {
    "number": 18894004,
    "time": "05/05/20(Tue)19:43:21",
    "subject": null,
    "original_post": "Bitcoin was blockchains first application. <br><br>Holo is holochains first application. <br><br>Holochain is vastly Superior to blockchain. <br><br>Early Holo hosts and investors are going to be loaded in a few years.",
    "replies": 7,
    "images": 2
  },
  {
    "number": 18894398,
    "time": "05/05/20(Tue)20:09:17",
    "subject": "I have $200,000 to spend",
    "original_post": "You have 10 posts to sell me your bags and maybe i will go all in",
    "replies": 26,
    "images": 2
  },
  {
    "number": 18893873,
    "time": "05/05/20(Tue)19:36:03",
    "subject": "Is 32 ETH the entry fee to the Citadel or the ETHnostate?",
    "original_post": "What does /biz/ call it?",
    "replies": 5,
    "images": 2
  },
  {
    "number": 18895208,
    "time": "05/05/20(Tue)20:59:03",
    "subject": "BTC prediction general",
    "original_post": "Will it break 10k or 8k first?",
    "replies": 3,
    "images": 0
  },
  {
    "number": 18894335,
    "time": "05/05/20(Tue)20:05:09",
    "subject": "FUCK YOU",
    "original_post": "every time I buy something shilled here... I lose money...<br>Toxic faggots<br>FUCK you...",
    "replies": 16,
    "images": 4
  },
  {
    "number": 18894491,
    "time": "05/05/20(Tue)20:15:04",
    "subject": null,
    "original_post": "One word",
    "replies": 4,
    "images": 2
  },
  {
    "number": 18877910,
    "time": "05/05/20(Tue)05:57:00",
    "subject": null,
    "original_post": "Soon.",
    "replies": 138,
    "images": 18
  },
  {
    "number": 18892067,
    "time": "05/05/20(Tue)17:55:17",
    "subject": "Zil",
    "original_post": "Quietly doubles over the last month. Here&#039;s a tip for you degenerate gamblers: look at the volume increase and ask why. Then go look at who they hired a few weeks ago. You&#039;re fucking welcome. This is going to be 4 cents by the end of May.",
    "replies": 18,
    "images": 0
  },
  {
    "number": 18894010,
    "time": "05/05/20(Tue)19:43:34",
    "subject": null,
    "original_post": "The current economy system is a big ponzi scam where current generations profit but future ones 100+ years get fucked.",
    "replies": 9,
    "images": 0
  },
  {
    "number": 18895189,
    "time": "05/05/20(Tue)20:57:29",
    "subject": "LINK SCAMMER BTFO",
    "original_post": "THEY ARE CRUMBLING AHAHAHAHAHAHAHAAHAHAAHA",
    "replies": 1,
    "images": 0
  },
  {
    "number": 18893316,
    "time": "05/05/20(Tue)19:05:05",
    "subject": null,
    "original_post": "How much do you get paid bi-weekly and what is your monthly rent payment?",
    "replies": 49,
    "images": 4
  },
  {
    "number": 18891313,
    "time": "05/05/20(Tue)17:20:39",
    "subject": "/PTG/ penny stocks general",
    "original_post": "/PTG/ - After hours crab edition<br><br>Old thread: <a href=\"/biz/thread/18887493#p18887493\" class=\"quotelink\">&gt;&gt;18887493</a>",
    "replies": 186,
    "images": 26
  },
  {
    "number": 18891663,
    "time": "05/05/20(Tue)17:36:45",
    "subject": "/tsg/ Tanker Stock General",
    "original_post": "It&#039;s hard to tell that DHT is a profitable company looking at its stock edition<br><br><span class=\"quote\">&gt;Education</span><br>https://www.investopedia.com/articl<wbr>es/investing/012316/crude-tankers-b<wbr>usiness-transporting-oil.asp<br>https://lawexplores.com/the-tanker-<wbr>market-current-structure-and-econom<wbr>ic-analysis/<br>https://blogs.worldbank.org/develop<wbr>menttalk/what-triggered-oil-price-p<wbr>lunge-2014-2016-and-why-it-failed-d<wbr>eliver-economic-impetus-eight-chart<wbr>s<br><br><span class=\"quote\">&gt;Maritime/tanker news</span><br>https://lloydslist.maritimeintellig<wbr>ence.informa.com/<br>https://www.tradewindsnews.com/tank<wbr>ers/<br>https://www.hellenicshippingnews.co<wbr>m/<br>https://www.marinevesseltraffic.com<wbr>/2013/02/tanker-track.html<br><br><span class=\"quote\">&gt;Companies (not exhaustive or recommendations)</span><br>https://www.frontline.bm/<br>https://www.tenn.gr/<br>https://www.euronav.com/<br>https://www.dhtankers.com/<br>https://www.nat.bm/<br>https://www.teekay.com/business/tan<wbr>kers/<br>https://www.scorpiotankers.com<br>https://www.sflcorp.com/<br><br><span class=\"quote\">&gt;Past earnings report</span><br>ASC : Estimated EPS $0.14, actual $0.20 (best on record).<br>DHT: Estimated EPS $0.54, actual $0.44 (dwarfed 2019 Q1 of $0.12).<br><br><span class=\"quote\">&gt; Earnings report expected today </span><br>None<br><br><span class=\"quote\">&gt; Upcoming earnings reports calendar</span><br>STNG tomorrow, pre-market<br>EURN on 5/7 (time not specified)<br>FRO on 5/14, pre-market <br>NAT on 5/18 (time not specified)<br>TNK on 5/21, pre-market<br>SFL on 6/2 (time not specified)<br>TNP on 6/4, pre-market <br><br><span class=\"quote\">&gt;Another important date </span><br>May 19th, 2020 (you know why)<br><br>Previous thread:<br><a href=\"/biz/thread/18881534#p18881534\" class=\"quotelink\">&gt;&gt;18881534</a>",
    "replies": 94,
    "images": 24
  },
  {
    "number": 18895033,
    "time": "05/05/20(Tue)20:47:03",
    "subject": null,
    "original_post": "<span class=\"quote\">&gt;3.66</span>",
    "replies": 4,
    "images": 0
  },
  {
    "number": 18893353,
    "time": "05/05/20(Tue)19:07:11",
    "subject": null,
    "original_post": "Looks like landlords are going to start having to get a job soon. :^)<br>What will they put on their resume?",
    "replies": 16,
    "images": 3
  },
  {
    "number": 18895184,
    "time": "05/05/20(Tue)20:57:16",
    "subject": null,
    "original_post": "I&#039;d like to have a more philosophical conversation about HEX. I&#039;m not advocating or opposing it, I&#039;d just like to hear your thoughts. In fact this isn&#039;t even aimed at HEX but the thesis behind it.<br><br>I believe the reason that people invest in crypto is twofold:<br><span class=\"quote\">&gt;Alternate store of wealth.</span><br><span class=\"quote\">&gt;Investment into shares of the project i.e. altcoins and what they suggest to bring to the table fundamentally a la society.</span><br><br>Crypto still has little adoption, in fact close to zero adoption or use case after a decade and it is decreasing.<br><br>If HEX&#039;s ideas are to be followed through; as explicitly an investment that was invented with the singular purpose of investing (w/ CD structure as this potential big drop leverage), then does that say anything to many altcoins, and cryptocurrency as a whole?<br><br>Would HEX&#039;s potential success as this market disruptor amount to a zero sum game against all other crypto&#039;s? And importantly, do people actually want this potentially safer style of investment or do they actually prefer (consciously or not) investing in crypto as they have been since advent - as the highly volatile, big risk big reward side bet. The riskier S&amp;P500. <br><br>Is HEX essentially saying that it&#039;s time to brush aside mass adoption/crypto as everyday currency? But this could be a seismic shift in the space, destroying part of what made crypto crypto. Could this hurt or kill crypto?",
    "replies": 0,
    "images": 0
  },
  {
    "number": 18894384,
    "time": "05/05/20(Tue)20:08:27",
    "subject": null,
    "original_post": "AND JUS LIKE THAT, BITCOIN WILL NEVER EVER EVER BE BELOW $9000 EVER AGAIN",
    "replies": 7,
    "images": 3
  },
  {
    "number": 18893459,
    "time": "05/05/20(Tue)19:13:20",
    "subject": null,
    "original_post": "<span class=\"quote\">&gt;If you give everyone $1200 then everyone will just raise their prices by $1200. It&#039;s inflation bro. Learn economics.</span><br><br>How come this hasn&#039;t happened yet? The &quot;experts&quot; promised us this is what would happen if the government gave everyone free money. Is there any proof that UBI or raising the minimum wage actually contributes to inflation? All the corporations know that Americans have an extra $1200 in their pockets so why haven&#039;t they all just randomly raised their prices just cause they can!!!",
    "replies": 51,
    "images": 5
  },
  {
    "number": 18883381,
    "time": "05/05/20(Tue)11:39:08",
    "subject": null,
    "original_post": "so this thing really got exposed huh? Sold my 6k just now thanks to the schizo anon who posted all the proof",
    "replies": 90,
    "images": 11
  },
  {
    "number": 18894732,
    "time": "05/05/20(Tue)20:29:04",
    "subject": null,
    "original_post": "MAKE IT STOP",
    "replies": 10,
    "images": 2
  },
  {
    "number": 18894947,
    "time": "05/05/20(Tue)20:41:38",
    "subject": "horizen",
    "original_post": "Why is it worth 5 dollars?",
    "replies": 1,
    "images": 0
  },
  {
    "number": 18893856,
    "time": "05/05/20(Tue)19:35:01",
    "subject": null,
    "original_post": "If you had $1000 of credit card rebates to spend on anything you want, what would you spend it on? <br><br>I don’t know if I should pay my electricity bill for the next few months or buy a dishwasher",
    "replies": 5,
    "images": 1
  },
  {
    "number": 18894012,
    "time": "05/05/20(Tue)19:43:42",
    "subject": "BREAKING NEWS Qnt... No CBDC&#039;s",
    "original_post": "Qnt... no Cbdc&#039;s<br><br>Jesus Christ <br>It was all made up",
    "replies": 4,
    "images": 0
  },
  {
    "number": 18886670,
    "time": "05/05/20(Tue)14:15:07",
    "subject": "BTC will lose #1 in market cap 2020",
    "original_post": null,
    "replies": 55,
    "images": 6
  },
  {
    "number": 18895051,
    "time": "05/05/20(Tue)20:48:23",
    "subject": "Is this the next 100x?",
    "original_post": null,
    "replies": 2,
    "images": 0
  },
  {
    "number": 18893313,
    "time": "05/05/20(Tue)19:04:52",
    "subject": null,
    "original_post": "Is there a way to make money from being proficient in AE? It’s soemthing I enjoy doing but current job(graphic design) dosent really require it.<br>And don’t say fiverr because then I’m competing against a bunch of Indians who will do it for pennies.",
    "replies": 5,
    "images": 0
  },
  {
    "number": 18891670,
    "time": "05/05/20(Tue)17:37:07",
    "subject": null,
    "original_post": "Should more women learn to code?",
    "replies": 37,
    "images": 3
  },
  {
    "number": 18895119,
    "time": "05/05/20(Tue)20:53:10",
    "subject": "You should EDI",
    "original_post": "<span class=\"quote\">&gt;240k market cap.</span>",
    "replies": 0,
    "images": 0
  },
  {
    "number": 18872034,
    "time": "05/04/20(Mon)21:04:59",
    "subject": "Idena - The Ultimate Breadcrumb",
    "original_post": "Hi Newfags, 2012 btc oldfag here. I&#039;m here to share some advice and pass on a lesson.<br><br>A bit about my history. I first purchased BTC in single digits in early 2012. I didn&#039;t do it for investment purposes and I definitely didn&#039;t know it would ever x2 in value or let alone x10,000 in value from when I purchased it. Why did I buy it? It was a necessary means of exchange to purchase on SR 1.0. This was BTC&#039;s first ever real use case. But that isn&#039;t the point of this post. What I did learn however, was a valuable lesson when I saw the price go from $2 to $100+ - I thought why? It was only then that I discovered the magic underneath bitcoin, its blockchain and ability to remove the middle man and allow you to store wealth outside of a silo&#039;s - silo&#039;s of banks and government control - protection through decentralisation via a peer to peer network. No one could take this from you as long as you kept your private key, your btc was safe. <br><br>Now you have the background, let&#039;s move away from money, onto a topic just as big &#039;identity&#039;. When the internet was built, it was built without human identity layer, instead IP addresses define computers on a network, not people on a network - this is worth repeating, there is no human identity layer on the internet and there is no efficient way to prove you&#039;re a human on the internet. The issue with this, is you have multiple identities instead of a single identity. You have an identity with facebook, another identity with google and another with Amazon etc. You have hundreds of passwords and none of your identities are able to be shared between these companies, you need to start over again and again. Have you ever thought how annoying it is when you&#039;ve spent years building up a trustworthy profile on your chosen website / game / forum only to have to start all over again? <br><br>The problem? Identity lives in silo&#039;s on the internet. Google isn&#039;t going to share your identity with Amazon, and neither will Amazon share your identity with Steam.",
    "replies": 89,
    "images": 13
  },
  {
    "number": 18878858,
    "time": "05/05/20(Tue)07:26:29",
    "subject": "/PMG/ precious metals general",
    "original_post": "Bullion Dealers<br><br>https://www.apmex.com/<br>https://www.boldpreciousmetals.com/<wbr><br>https://www.bgasc.com/<br>https://www.gainesvillecoins.com/<br>https://www.jmbullion.com/<br>https://www.providentmetals.com/<br>https://www.silvertowne.com/<br>https://sdbullion.com/<br>https://schiffgold.com/<br>https://goldsilver.com/<br>https://pinehurstcoins.com/<br>https://www.sprottmoney.com/<br>https://www.moneymetals.com/<br>https://monumentmetals.com/<br>https://www.goldenstatemint.com/<br>https://goldsilver.be/en/<br>https://www.muenze-berlin.de/<br>https://www.hollandgold.nl/<br>https://www.europesilverbullion.com<wbr>/<br>https://www.celticgold.eu/en/<br>https://www.muenzeoesterreich.at/en<wbr>g/<br><br><span class=\"quote\">&gt;Compare</span><br>https://findbullionprices.com/<br><br><span class=\"quote\">&gt;News</span><br>https://www.kitco.com/<br>http://silverseek.com/<br>https://www.mining.com/<br><br><span class=\"quote\">&gt;Bullion tax info by state:</span><br>https://www.apmex.com/state-sales-t<wbr>ax-information<br><br><span class=\"quote\">&gt;Prospecting</span><br>https://www.youtube.com/watch?v=ZCL<wbr>6FKQZyoM [Open] [Open] [Embed] [Embed] [Open]<br>https://www.usgs.gov/energy-and-min<wbr>erals/mineral-resources-program/sci<wbr>ence<br>https://www2.gov.bc.ca/assets/gov/f<wbr>arming-natural-resources-and-indust<wbr>ry/mineral-exploration-mining/docum<wbr>ents/mineral-titles/mt-faqs/faq_fmc<wbr>.pdf<br>https://www.mndm.gov.on.ca/en/mines<wbr>-and-minerals/mining-act<br>https://www.amazon.ca/Gold-Creeks-G<wbr>hostowns-British-Columbia/dp/088839<wbr>988X<br><br><span class=\"quote\">&gt;Test</span><br>Nitric Acid<br>https://www.youtube.com/watch?v=3mg<wbr>9YcAShTo [Open] [Open]<br>Magnets, how do they work?<br>https://www.youtube.com/watch?v=NgS<wbr>Xg-WOEVY [Open] [Open]<br><br><span class=\"quote\">&gt;YouTube/Podcasts</span><br>https://www.youtube.com/user/silver<wbr>guru David Morgan<br>https://www.youtube.com/user/Sprott<wbr>Global<br>https://www.youtube.com/user/KitcoN<wbr>ews<br>https://www.youtube.com/channel/UCq<wbr>mToXM7x2tD7-2rs0KvObA Silver Bullion TV<br>https://www.youtube.com/channel/UCX<wbr>PvtSNFvh9FJrwN02crJ_A money metals exchange podcast<br>https://www.youtube.com/user/whygol<wbr>dandsilver mike maloney&#039;s channel<br>https://www.youtube.com/channel/UCl<wbr>zSFvylrK8ij3KVwrHzjdA As Good As Gold Australia",
    "replies": 116,
    "images": 34
  },
  {
    "number": 18894293,
    "time": "05/05/20(Tue)20:02:08",
    "subject": "WHAT THE HEX WAS THAT?!?!?!?!",
    "original_post": null,
    "replies": 13,
    "images": 1
  },
  {
    "number": 18891949,
    "time": "05/05/20(Tue)17:49:22",
    "subject": "/BATG/ Basic Attention Token General: Payday Edition",
    "original_post": "Its payday, Lads! What did you earn this month? <br>Let&#039;s talk some BAT/Brave.",
    "replies": 43,
    "images": 16
  },
  {
    "number": 18893012,
    "time": "05/05/20(Tue)18:46:34",
    "subject": null,
    "original_post": "The scy boys are in",
    "replies": 12,
    "images": 4
  },
  {
    "number": 18895048,
    "time": "05/05/20(Tue)20:48:11",
    "subject": "I sold 12 hours ago and am fucking seething right now",
    "original_post": "I thought I was doing the smart thing anons. I took my 50% in 10 days gain and sold. I got burned by VIDT because I held through the vote. I got dumped on so fucking hard that I took the gains this time and took my gain. <br><span class=\"quote\">&gt; Now it’s mooning</span>",
    "replies": 0,
    "images": 0
  },
  {
    "number": 18894822,
    "time": "05/05/20(Tue)20:34:41",
    "subject": null,
    "original_post": "<span class=\"quote\">&gt;he went all in on a literal botnet</span>",
    "replies": 10,
    "images": 0
  },
  {
    "number": 18895041,
    "time": "05/05/20(Tue)20:47:31",
    "subject": "xDai Stake - Bitmax Fund&#039;s First Investment - $700K Marketcap",
    "original_post": "This has been shilled by the likes of Ethereum co-founders Joseph Lubin and Gavin Wood along with Anthony Pompliano. In a nutshell xDai is the world&#039;s first USD pegged stable platform brought to you by the POA and Maker DAO guys. It runs as an ETH sidechain using POS so you can make lightning fast transactions alongside being able to build scalable decentralized applications with a predictable and stable native currency. This was the rage at ETHDenver last year. All of the food trucks at the event ran a total of about $38K in xDAI transactions at a total fee of $0.20. Additionally Silicon Valley data firm, Splunk, used xDai to build a native currency for their own conference in 2019. Splunk is currently sitting at a marketcap of $22.8 billion. There are also many other dapps that have gone live on the platform recently as well as community inclusive currencies that are currently being used in Kenya. This might be the biggest gem out there at the moment. Do not sleep on it frens.",
    "replies": 0,
    "images": 0
  },
  {
    "number": 18888764,
    "time": "05/05/20(Tue)15:35:45",
    "subject": "/LITGEN/ Lition General",
    "original_post": "Based edition",
    "replies": 53,
    "images": 35
  },
  {
    "number": 18892386,
    "time": "05/05/20(Tue)18:11:10",
    "subject": null,
    "original_post": "Bitcoin breaks out to 10,400 tonight. If you open a 100x long with 100 dollars you’ll make $1600. This is so easy to tell looking at the chart. DYOR AND SCREENSHOT THIS",
    "replies": 25,
    "images": 2
  },
  {
    "number": 18893166,
    "time": "05/05/20(Tue)18:55:35",
    "subject": null,
    "original_post": "What&#039;s the moment when you finally understand the value of Bitcoin/Crypto? <br>What made that idea click to you?",
    "replies": 8,
    "images": 1
  },
  {
    "number": 18894160,
    "time": "05/05/20(Tue)19:53:11",
    "subject": "Virgin Galactic is partnering with NASA to develop supersonic point-to-point air travel",
    "original_post": "https://techcrunch.com/2020/05/05/v<wbr>irgin-galactic-is-partnering-with-n<wbr>asa-to-develop-supersonic-point-to-<wbr>point-air-travel/<br><br>Pretty big news, get SPCE while its still under $20",
    "replies": 6,
    "images": 0
  },
  {
    "number": 18886737,
    "time": "05/05/20(Tue)14:17:30",
    "subject": "Let me get this straight",
    "original_post": "Over 50% of COVID deaths in UK/Europe are from care homes.<br>Average length of stay in a care home before death of natural causes is 800 days.<br>We have caused untold damage, will have record levels of economic difficulty/unemployment, and businesses close on record numbers without the governments of Europe able to bail them all out just so some coffin dodgers could live an extra 800 days in the best case scenario?<br><br>I cant tell if this is a fucking dream or real life. This makes no sense to me anymore.<br><br>UK in particular seems to be trying to avoid easing lockdowns as long as possible, like they dont want to avoid economic collapse.",
    "replies": 72,
    "images": 16
  },
  {
    "number": 18893452,
    "time": "05/05/20(Tue)19:12:36",
    "subject": "NWC TO 5 CENTS",
    "original_post": "Time to load up on cheap NWC",
    "replies": 8,
    "images": 0
  },
  {
    "number": 18893619,
    "time": "05/05/20(Tue)19:20:47",
    "subject": null,
    "original_post": "are you all ready for the post halving dump?<br><br>anon? are you? did you buy the rumor?",
    "replies": 4,
    "images": 1
  },
  {
    "number": 18894234,
    "time": "05/05/20(Tue)19:58:17",
    "subject": null,
    "original_post": "<span class=\"quote\">&gt;tfw anti Semitic</span>",
    "replies": 11,
    "images": 3
  },
  {
    "number": 18894343,
    "time": "05/05/20(Tue)20:05:31",
    "subject": null,
    "original_post": "<span class=\"quote\">&gt;Now is obviously bull trapping</span><br><span class=\"quote\">&gt;Putting all your money to the stonk market</span><br><br>Why would you do that biz?",
    "replies": 10,
    "images": 1
  },
  {
    "number": 18891732,
    "time": "05/05/20(Tue)17:39:44",
    "subject": "OIL PUMP: WHEN?",
    "original_post": "TOMORROW. SEE YOU THERE.",
    "replies": 20,
    "images": 1
  },
  {
    "number": 18893460,
    "time": "05/05/20(Tue)19:13:21",
    "subject": null,
    "original_post": "<span class=\"quote\">&gt;klonopin binge</span><br><span class=\"quote\">&gt;come to senses</span><br><span class=\"quote\">&gt;down 3 mil</span>",
    "replies": 9,
    "images": 0
  },
  {
    "number": 18894780,
    "time": "05/05/20(Tue)20:32:19",
    "subject": null,
    "original_post": "How many BTC to &quot;Make it&quot; by 2023? (3 Million USD value)",
    "replies": 4,
    "images": 0
  },
  {
    "number": 18894865,
    "time": "05/05/20(Tue)20:37:01",
    "subject": null,
    "original_post": "FED keeps printing trillions and trillions of dollars. Are there no consequences for this? What is money anyway? Is dollar just worthless in long run? Trump is bragging about dollar being so strong, hence no consequences. but for how long?",
    "replies": 0,
    "images": 0
  },
  {
    "number": 18894855,
    "time": "05/05/20(Tue)20:36:34",
    "subject": null,
    "original_post": "I have saved up 5000 and want to buy a car cash at a car lot that is like 4000 (but after taxes and registration I think it it will basically be 5000). My friend said I should buy it with my credit card I never used because I despise borrowing money. But if I have the cash to pay it off will it help my credit if I just pay off the card when the payment is due?",
    "replies": 0,
    "images": 0
  },
  {
    "number": 18889479,
    "time": "05/05/20(Tue)15:56:51",
    "subject": "GET INTO LCX NOW RETARDS",
    "original_post": null,
    "replies": 29,
    "images": 8
  },
  {
    "number": 18894795,
    "time": "05/05/20(Tue)20:33:12",
    "subject": "Chromia binance listing",
    "original_post": "Get ready. It will pump until 11pm",
    "replies": 0,
    "images": 0
  },
  {
    "number": 18893971,
    "time": "05/05/20(Tue)19:41:38",
    "subject": null,
    "original_post": "WTF why has the middle class gotten lazier over time? If they worked harder they would be paid more! This proves that boomers really were the best generation.",
    "replies": 5,
    "images": 0
  },
  {
    "number": 18893204,
    "time": "05/05/20(Tue)18:57:55",
    "subject": null,
    "original_post": "<span class=\"quote\">&gt;Tfw missed out on HEX</span>",
    "replies": 45,
    "images": 7
  },
  {
    "number": 18892937,
    "time": "05/05/20(Tue)18:42:38",
    "subject": null,
    "original_post": "Bitcoin is a scam, buy gold",
    "replies": 12,
    "images": 4
  },
  {
    "number": 18891332,
    "time": "05/05/20(Tue)17:21:39",
    "subject": "Is /pol/ allowed in the citadel?",
    "original_post": "<a href=\"//boards.4chan.org/pol/thread/256319872#p256319872\" class=\"quotelink\">&gt;&gt;&gt;/pol/256319872</a>",
    "replies": 17,
    "images": 4
  },
  {
    "number": 18894247,
    "time": "05/05/20(Tue)19:59:00",
    "subject": null,
    "original_post": "So after the economy fully reopens and the housing market collapses, is it going to be in favor of people looking to buy houses/land or against?<br>Assuming great credit and a sizeable down payment of course.",
    "replies": 2,
    "images": 0
  },
  {
    "number": 18892301,
    "time": "05/05/20(Tue)18:06:48",
    "subject": null,
    "original_post": "https://torontostoreys.com/cibc-can<wbr>adian-home-prices-forecast/<br><br>WE ALL FALL DOWN LIKE TOY SOLDIERS<br><br>RIP TORONTO",
    "replies": 8,
    "images": 0
  },
  {
    "number": 18894715,
    "time": "05/05/20(Tue)20:27:46",
    "subject": "Who should win?",
    "original_post": "https://www.strawpoll.me/19957634/",
    "replies": 2,
    "images": 1
  },
  {
    "number": 18894714,
    "time": "05/05/20(Tue)20:27:34",
    "subject": "Which one is /biz taking?",
    "original_post": null,
    "replies": 1,
    "images": 0
  },
  {
    "number": 18894646,
    "time": "05/05/20(Tue)20:23:30",
    "subject": null,
    "original_post": "<span class=\"quote\">&gt;*snib*</span><br><span class=\"quote\">&gt;8800</span><br><span class=\"quote\">&gt;9050</span><br><span class=\"quote\">&gt;8800</span><br><span class=\"quote\">&gt;9050</span><br><span class=\"quote\">&gt;8800</span><br><span class=\"quote\">&gt;9050</span><br><span class=\"quote\">&gt;*snib*</span>",
    "replies": 2,
    "images": 2
  },
  {
    "number": 18891039,
    "time": "05/05/20(Tue)17:07:16",
    "subject": null,
    "original_post": "What is the value proposition that drives the hiring of minorities and women?",
    "replies": 23,
    "images": 4
  },
  {
    "number": 18891055,
    "time": "05/05/20(Tue)17:08:14",
    "subject": "RLC:",
    "original_post": "This is a RLC thread.",
    "replies": 6,
    "images": 1
  },
  {
    "number": 18893867,
    "time": "05/05/20(Tue)19:35:42",
    "subject": "Pajeet vs Ahmed",
    "original_post": "Do they have crypto gang violence in India? Are there roaming clouds of shit that collide and just start throwing coins all over the place? Do they attack wifi towers in rival coin’s turf and leave a pile of their worthless shitcoins to mark their work? Do they pillage and burn their enemy’s meme stashes while they’re away spamming on /biz/?<br><br>Most importantly, how can i profit off this",
    "replies": 1,
    "images": 0
  },
  {
    "number": 18894645,
    "time": "05/05/20(Tue)20:23:29",
    "subject": null,
    "original_post": "Putting economic policy before fiscal responsibility is like putting the cart before the horse.",
    "replies": 0,
    "images": 0
  },
  {
    "number": 18894612,
    "time": "05/05/20(Tue)20:21:20",
    "subject": null,
    "original_post": "<span class=\"quote\">&gt;tfw not paying many attention to stocks and YOLOing all my money on shitcoins like ETH </span><br><br>man I hope this works out",
    "replies": 2,
    "images": 0
  },
  {
    "number": 18892079,
    "time": "05/05/20(Tue)17:55:36",
    "subject": null,
    "original_post": "<span class=\"quote\">&gt;mfw I had no money as child to buy all the stuff I wanted and now having money but no interest in it anymore</span><br><br>Why is does it have to be like this?",
    "replies": 15,
    "images": 5
  },
  {
    "number": 18885261,
    "time": "05/05/20(Tue)13:08:14",
    "subject": "What&#039;s the next 100x cryptogem?",
    "original_post": "Please unironical answers only",
    "replies": 27,
    "images": 4
  },
  {
    "number": 18893616,
    "time": "05/05/20(Tue)19:20:43",
    "subject": "I&#039;ll just leave this here...",
    "original_post": null,
    "replies": 20,
    "images": 3
  },
  {
    "number": 18894001,
    "time": "05/05/20(Tue)19:43:13",
    "subject": null,
    "original_post": "I come here to shit on linkies and nothing else.",
    "replies": 9,
    "images": 1
  },
  {
    "number": 18886675,
    "time": "05/05/20(Tue)14:15:11",
    "subject": "indoor rancher general",
    "original_post": "how my fellow indoor ranchers doin today?",
    "replies": 84,
    "images": 22
  },
  {
    "number": 18892591,
    "time": "05/05/20(Tue)18:23:51",
    "subject": null,
    "original_post": "I&#039;ve only been learning how to trade for about a week yet I already feel smarter than half this board<br><br>Is that a sign that I&#039;m actually much dumber than I think I am, or is this board just very stupid",
    "replies": 24,
    "images": 2
  },
  {
    "number": 18886997,
    "time": "05/05/20(Tue)14:25:59",
    "subject": null,
    "original_post": "Good shit Skyjeets, good thing I listened and bought a bag,<br>ready for the imminent run back to $3usd, hold me tight.",
    "replies": 43,
    "images": 11
  },
  {
    "number": 18894551,
    "time": "05/05/20(Tue)20:17:47",
    "subject": null,
    "original_post": "if you could choose just ONE, which would you pick, FTM or DAG?",
    "replies": 0,
    "images": 0
  },
  {
    "number": 18894106,
    "time": "05/05/20(Tue)19:49:32",
    "subject": null,
    "original_post": "Inversed Jim and now I&#039;m broke. Fuck you biz.",
    "replies": 2,
    "images": 0
  },
  {
    "number": 18885257,
    "time": "05/05/20(Tue)13:07:59",
    "subject": "Is it worth buying?",
    "original_post": "Guys at what point should you buy one of these?",
    "replies": 59,
    "images": 2
  },
  {
    "number": 18894282,
    "time": "05/05/20(Tue)20:01:26",
    "subject": "We are all going to make it.",
    "original_post": "<span class=\"quote\">&gt;Work in the U.S and save money</span><br><span class=\"quote\">&gt;go to Serbia/Slovakia/Russia/Ukraine etc.</span><br><span class=\"quote\">&gt;buy houses/apartments</span><br><span class=\"quote\">&gt;rent them out</span><br><span class=\"quote\">&gt;live off of the passive income like a king with extra money left over for travel, going out, making a home gym etc.</span><br>Apartments in Eastern Europe are between $50,000-150,000. Monthly expenses are around $600-1000, rent included ($300). How is this not an out for people stuck in the U.S, completely blackpilled on women and culture?<br>United States has been turned into an economic zone, stripped of any culture and spiritual meaning. You are aware of this, which puts you ahead of the most. Make the best of it if you are still young, I know I am.",
    "replies": 1,
    "images": 0
  },
  {
    "number": 18894327,
    "time": "05/05/20(Tue)20:04:31",
    "subject": null,
    "original_post": "<span class=\"quote\">&gt;BTC was around $210 at the time of the post</span><br><br>Do you think OP made it?",
    "replies": 3,
    "images": 0
  },
  {
    "number": 18894219,
    "time": "05/05/20(Tue)19:57:07",
    "subject": "Lition",
    "original_post": "Every Lition Thread died all at once, remind me how this isn&#039;t a Satsgang PnD again?",
    "replies": 3,
    "images": 0
  },
  {
    "number": 18893408,
    "time": "05/05/20(Tue)19:10:28",
    "subject": null,
    "original_post": "how much does this girl make from streaming? thinking of finding myself a gf to whore out to nerds on twitch to make some income",
    "replies": 16,
    "images": 4
  },
  {
    "number": 18891246,
    "time": "05/05/20(Tue)17:17:15",
    "subject": "What happens when you make it?",
    "original_post": "I keep wondering. What I would do when I would make it. And I have not a clue...What would do frens?<br>Fuck escorts?<br>Get a massive house?<br>Tell me.",
    "replies": 32,
    "images": 2
  },
  {
    "number": 18894272,
    "time": "05/05/20(Tue)20:00:42",
    "subject": null,
    "original_post": "I know it&#039;s a scam but godamn I&#039;m going to ride it until the last possible second",
    "replies": 9,
    "images": 3
  },
  {
    "number": 18894379,
    "time": "05/05/20(Tue)20:08:00",
    "subject": null,
    "original_post": "Stop shilling this fucking stinker, it’s not going anywhere. Enjoy your bags.",
    "replies": 1,
    "images": 1
  },
  {
    "number": 18887858,
    "time": "05/05/20(Tue)14:58:34",
    "subject": null,
    "original_post": "stop feeding the parasite that is Blockstream. don&#039;t buy Bitcoin.",
    "replies": 72,
    "images": 16
  },
  {
    "number": 18894046,
    "time": "05/05/20(Tue)19:45:59",
    "subject": "absolute state of decred",
    "original_post": "<span class=\"quote\">&gt;muh hedge to btc</span><br><br>dcr/btc only going down<br><br><span class=\"quote\">&gt;muh decentralized governance and treasury</span><br><br>approved only shit proposals bc stakeholders are brainlets<br><br><span class=\"quote\">&gt;muh DEX</span><br><br>carrot on the stick by devs<br><br><span class=\"quote\">&gt;decred</span><br><br>dickred",
    "replies": 3,
    "images": 0
  },
  {
    "number": 18894142,
    "time": "05/05/20(Tue)19:52:10",
    "subject": null,
    "original_post": "I&#039;m so tired of life and so tired of being poor. What the fuck do I do? Honestly considering suicide at this point",
    "replies": 1,
    "images": 0
  },
  {
    "number": 18894341,
    "time": "05/05/20(Tue)20:05:28",
    "subject": null,
    "original_post": "Do you over leverage or do you<br>under leverage? Im more of a mid leverager myself I just want /biz/&#039;s opinion",
    "replies": 2,
    "images": 0
  },
  {
    "number": 18894351,
    "time": "05/05/20(Tue)20:06:12",
    "subject": null,
    "original_post": "ITS OVER NINE THOUSAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA<wbr>AAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAN<wbr>D",
    "replies": 0,
    "images": 0
  },
  {
    "number": 18892684,
    "time": "05/05/20(Tue)18:28:37",
    "subject": "NAV",
    "original_post": "Post your net asset value<br>Cash and equivalents: ~$30k<br>IRA (Vanguard growth index fund) ~$7300<br>401k (some 2045 target retirement fund) ~$12000<br>2013 Honda Civic loan -$3000<br><br>$46,300",
    "replies": 9,
    "images": 3
  },
  {
    "number": 18893918,
    "time": "05/05/20(Tue)19:38:44",
    "subject": null,
    "original_post": "Sergey Speaks Tomorrow. <br>Little Pump and Major Dump.<br>Halvening Occurs 22x Pump.<br>Slowly dumps over time.",
    "replies": 6,
    "images": 0
  },
  {
    "number": 18891571,
    "time": "05/05/20(Tue)17:32:49",
    "subject": "/smg/ - Stock Market General",
    "original_post": "South Sea Bubble of 1720<br><br><span class=\"quote\">&gt;Brokers</span><br>https://pastebin.com/F1yujtVq<br><br><span class=\"quote\">&gt;Stock market Words</span><br>https://pastebin.com/VtnpN5iJ<br><br><span class=\"quote\">&gt;Risk Management</span><br>https://pastebin.com/sqJUcbjp<br><br><span class=\"quote\">&gt;Live Bloomberg Stream</span><br>http://www.livenewson.com/american/<wbr>bloomberg-television-business.html<br><br><span class=\"quote\">&gt;Educational Sites</span><br>https://www.investopedia.com/<br>https://www.khanacademy.org/economi<wbr>cs-finance-domain<br>https://nhentai.net/tag/crossdressi<wbr>ng/<br><br><span class=\"quote\">&gt;Free Charts</span><br>http://www.tradingview.com<br>https://www.finscreener.com/<br><br><span class=\"quote\">&gt;Screeners</span><br>https://finviz.com/<br>https://www.tradingview.com/screene<wbr>r<br>https://etfdb.com/<br><br><span class=\"quote\">&gt;Pre-Market Data and Live Data</span><br>https://www.investing.com/indices/i<wbr>ndices-futures<br>https://finance.yahoo.com/<br><br><span class=\"quote\">&gt;Bio-pharma Catalyst Calendar</span><br>https://biopharmcatalyst.com<br><br><span class=\"quote\">&gt;Boomer Investing 101</span><br>https://www.bogleheads.org/wiki/Get<wbr>ting_started<br><br><span class=\"quote\">&gt;Dividend Reinvestment (DRIP) Calculator</span><br>https://www.dividendchannel.com/dri<wbr>p-returns-calculator/<br><br><span class=\"quote\">&gt;List of hedge fund holdings</span><br>https://fintel.io/<br><br><span class=\"quote\">&gt;Misc</span><br>https://squeezemetrics.com/monitor<br>https://market24hclock.com/<br><br><a href=\"/biz/thread/18889964#p18889964\" class=\"quotelink\">&gt;&gt;18889964</a>",
    "replies": 344,
    "images": 65
  },
  {
    "number": 18892188,
    "time": "05/05/20(Tue)18:00:49",
    "subject": "XRP has officially cucked chainlink",
    "original_post": "is this what you wanted? :)",
    "replies": 34,
    "images": 3
  },
  {
    "number": 18894248,
    "time": "05/05/20(Tue)19:59:01",
    "subject": null,
    "original_post": "Waiting for at least a 40% pump this week on Sky.<br><br>Get ready and buy a bag before sky breaks out of this pennant.",
    "replies": 0,
    "images": 0
  },
  {
    "number": 18893472,
    "time": "05/05/20(Tue)19:13:51",
    "subject": "Where is 42 at?",
    "original_post": "I need some new mind bending fibonacci patterns.",
    "replies": 5,
    "images": 1
  },
  {
    "number": 18892149,
    "time": "05/05/20(Tue)17:59:11",
    "subject": null,
    "original_post": "It looks like things are beginning to stabilize. Is the Fed going to successfully print its way out of another disaster? If so what does this mean for the future?",
    "replies": 12,
    "images": 1
  },
  {
    "number": 18884678,
    "time": "05/05/20(Tue)12:39:58",
    "subject": "7 FIGURE MEDIA BUDGET",
    "original_post": "NON-LITIANS BTFO.<br><br>https://medium.com/@mstephenw5/liti<wbr>on-enters-brand-partnership-with-sp<wbr>arwelt-rtl-to-drive-blockchain-powe<wbr>red-green-energy-badb2e2ac023",
    "replies": 60,
    "images": 13
  },
  {
    "number": 18888444,
    "time": "05/05/20(Tue)15:22:51",
    "subject": "Something is brewing with Tellor TRB",
    "original_post": "500 ETH in volume today. Community call tomorrow - what will be revealed?",
    "replies": 9,
    "images": 0
  },
  {
    "number": 18894217,
    "time": "05/05/20(Tue)19:57:03",
    "subject": null,
    "original_post": "<span class=\"quote\">&gt;day 870 of the crypto bear market</span>",
    "replies": 2,
    "images": 1
  },
  {
    "number": 18891962,
    "time": "05/05/20(Tue)17:49:55",
    "subject": null,
    "original_post": "Am holding SQQQ and im getting real tired of this clown economy.<br><br>There&#039;s not gonna be some reverse split bullshit to punish us any further, right?",
    "replies": 15,
    "images": 0
  },
  {
    "number": 18893103,
    "time": "05/05/20(Tue)18:51:14",
    "subject": null,
    "original_post": "you now realize the Halfing will happen on Monday. have a nice day.",
    "replies": 5,
    "images": 3
  },
  {
    "number": 18893756,
    "time": "05/05/20(Tue)19:29:26",
    "subject": "Describe Chainlink using one image",
    "original_post": "Pic related",
    "replies": 8,
    "images": 7
  },
  {
    "number": 18893687,
    "time": "05/05/20(Tue)19:25:40",
    "subject": null,
    "original_post": "March sucked<br>April sucked<br>May is looking bad<br>when will things get better",
    "replies": 2,
    "images": 1
  },
  {
    "number": 18892694,
    "time": "05/05/20(Tue)18:29:00",
    "subject": "ETH",
    "original_post": "Can eth 100x in the next 2 years?",
    "replies": 11,
    "images": 0
  },
  {
    "number": 18892436,
    "time": "05/05/20(Tue)18:14:05",
    "subject": null,
    "original_post": "Is being a well off blue collar type the most comfy lifestyle?<br><br><span class=\"quote\">&gt;Cool tools</span><br><span class=\"quote\">&gt;Women love thugs, chads and country boys</span><br><span class=\"quote\">&gt;Skill set can&#039;t be outsourced</span><br><span class=\"quote\">&gt;Fun outdoor activities</span><br><span class=\"quote\">&gt;BBQ&#039;s</span>",
    "replies": 6,
    "images": 0
  },
  {
    "number": 18894186,
    "time": "05/05/20(Tue)19:55:14",
    "subject": "$ANTS AIRDROP THREAD",
    "original_post": "it&#039;s that time again, post eth addresses<br><br>What is $ANTS? Join the discord: /Fe3SXdU for more info and airdrops (happening now)<br>/Fe3SXdU",
    "replies": 0,
    "images": 0
  },
  {
    "number": 18893276,
    "time": "05/05/20(Tue)19:02:34",
    "subject": "This kills the Monero",
    "original_post": null,
    "replies": 4,
    "images": 1
  },
  {
    "number": 18892332,
    "time": "05/05/20(Tue)18:08:28",
    "subject": "??",
    "original_post": "??",
    "replies": 19,
    "images": 5
  },
  {
    "number": 18893521,
    "time": "05/05/20(Tue)19:15:50",
    "subject": "Does LN even work?",
    "original_post": "If LN is real I should be able to receive 1$ to send without insane fees.",
    "replies": 13,
    "images": 3
  },
  {
    "number": 18886652,
    "time": "05/05/20(Tue)14:14:34",
    "subject": "The Quant drop will be Epic",
    "original_post": "They couldn&#039;t even seal the deal with a binance listing. <br>Connected binance chain a year ago and still on idex.. kek<br>Binance laughed at them. Kek<br><br>What the fuck have they even done? <br><br>No proof of anything accomplished. <br><br>Even the new product interchange, didn&#039;t work on the demo and not one fucking piece of information on it from the team has come out.<br><br>Q2 is going to be a disaster",
    "replies": 111,
    "images": 25
  },
  {
    "number": 18893018,
    "time": "05/05/20(Tue)18:46:45",
    "subject": null,
    "original_post": "Chromia has about five hours of pumping left until the binance competition ends. Dump at least 10 minutes before the result because both contestants will hit all time low after the result is published.",
    "replies": 4,
    "images": 1
  },
  {
    "number": 18893358,
    "time": "05/05/20(Tue)19:07:34",
    "subject": null,
    "original_post": "i sweat to god if bitcoin dumps below 8600 one more time i am going 125x short. it can&#039;t just keep going up",
    "replies": 11,
    "images": 2
  },
  {
    "number": 18891405,
    "time": "05/05/20(Tue)17:24:55",
    "subject": null,
    "original_post": "CHECK HEX PRICES",
    "replies": 18,
    "images": 2
  },
  {
    "number": 18893517,
    "time": "05/05/20(Tue)19:15:42",
    "subject": "Tech business",
    "original_post": "based buisiness?<br>I thought about technician businesses like phone/computer service. Im sick of working for someone, 4real if i don’t make company then im must shoot myself lol",
    "replies": 3,
    "images": 0
  }
]
```


Parameter       | Type       | Description
----------------|------------|-------------
number          | int        | Post number.
time            | string     | Timestamp of posted message.
subject         | string     | Subject of post.
original_post   | string     | Original post.
replies         | int        | Number of replies.
images          | int        | Number of images.





## TwitterSearch

> Sample Data

```cli
{
  "keyword": "%24btc",
  "result_type": "popular",
  "tweet_count": "15"
}
```
Searches Twitter for tweets based on user inputs. Search is limited to 1 week history.

**Notes:**

* Search for tweets based on:

   * **Single-word:** Type any one word
   * **Multi-word:** To search for multi-words use %20 in between words; bitcoin%20ethereum%20litecoin = “bitcoin ethereum litecoin”
   * **Hash tag:** To search for hash tags add %23 in front of the text; %23bitcoin = #bitcoin
   * **@Username:** To search tweets with @Username in it, add %40 in front of the username; %40bitcoin = @bitcoin
   * **$crypto_ticker:** To search tweets with $crypto_ticker in it, add %24 in front of the ticker; %24btc = $btc
   * **From User:** To search for tweets from @Username, add from%3A in front of the username; from%3Abitcoin = tweets by @bitcoin


### Request Parameters

> Sample Request

```shell
curl -H "Accept: application/json" -H "Content-Type: application/json" -d '["%24btc","popular","15"]' https://api.maplenodes.com/xrs/TwitterSearch
```

<code class="api-call">TwitterSearch [keyword] [result_type] [tweet_count]</code>

Parameter       | Type       | Description
----------------|------------|-------------
keyword         | string     | Keyword to search.
result_type     | string     | Filter by: `recent`, `popular`, `mixed`.
tweet_count     | int        | Number of tweets to display (15-100).


### Response Parameters

<aside class="success">
200 OK
</aside>

> Sample 200 Response

```shell
[
  {
    "tweeted_by": "Binance",
    "@user": "binance",
    "tweet_time": "Mon May 04 22:30:30 +0000 2020",
    "tweet": "#BinanceFutures \"Top Traders\" positions on the daily time frame:\n\n$BTC Long 54.57%\n$ETH Long 51.26%\n$BCH Long 50.45%\n$XRP Long 51.12%\n$EOS Long 50.60%\n$LTC Long 51.43%\n$TRX Long 54.40%\n$ETC Long 51.62%\n$LINK Long 52.10%\n$XLM Long 57.78%\n\nTrade here:\n➡️ https://t.co/jkiHuCEZjO https://t.co/1NTikEkkWC",
    "retweet_count": 40,
    "favorite_count": 90
  },
  {
    "tweeted_by": "Kris Humphries",
    "@user": "KrisHumphries",
    "tweet_time": "Mon May 04 21:26:48 +0000 2020",
    "tweet": "How is everyone thinking the halving will affect $Link if at all? Will an increase in $BTC lift the price of all crypto assets?\n\n#chainlink #bitcoin #ethereum",
    "retweet_count": 44,
    "favorite_count": 351
  },
  {
    "tweeted_by": "The Wolf Of All Streets",
    "@user": "scottmelker",
    "tweet_time": "Tue May 05 16:13:26 +0000 2020",
    "tweet": "Chatter about the $BTC halving is giving me strong Y2K vibes.",
    "retweet_count": 50,
    "favorite_count": 287
  },
  {
    "tweeted_by": "Huobi",
    "@user": "HuobiGlobal",
    "tweet_time": "Tue May 05 04:51:50 +0000 2020",
    "tweet": "#Bitcoin just hit 9k! \n🤔Will $BTC hit $10k before the halving?",
    "retweet_count": 33,
    "favorite_count": 80
  },
  {
    "tweeted_by": "Huobi",
    "@user": "HuobiGlobal",
    "tweet_time": "Mon May 04 08:50:21 +0000 2020",
    "tweet": "#Huobi Futures accounts are 57% long $BTC/USD overall on the daily time frame.\n\nAre you a🐂or🐻on $BTC right now?\n\n⬇️ Trade on #HuobiFutures today!\n\nhttps://t.co/pBDEZPW48P",
    "retweet_count": 23,
    "favorite_count": 48
  },
  {
    "tweeted_by": "Crypto.com",
    "@user": "cryptocom",
    "tweet_time": "Thu Apr 30 05:35:54 +0000 2020",
    "tweet": "Presenting https://t.co/vCNztABJoG Halving Special, with 50% off on $BTC on 12 May on https://t.co/vCNztABJoG Exchange-$1M allocation- No CRO staking required🔥Sign up now! https://t.co/bq8A5wmHlw\nWe're also giving away $100K in #BTC. Follow &amp; RT for a chance to receive $250. https://t.co/6VoovyfDce",
    "retweet_count": 15539,
    "favorite_count": 13186
  },
  {
    "tweeted_by": "Independent Reserve",
    "@user": "indepreserve",
    "tweet_time": "Mon May 04 22:59:16 +0000 2020",
    "tweet": "The relative #Bitcoin market size compared to Gold, the US Federal Reserve balance sheet (including expected 2020 QE) and global currency supply.\n\n𝗬𝗼𝘂 𝗮𝗿𝗲 𝘀𝘁𝗶𝗹𝗹 𝗲𝗮𝗿𝗹𝘆. \n\nData courtesy of                 @glassnode \n\n$BTC https://t.co/Mg2O8NVU0B",
    "retweet_count": 43,
    "favorite_count": 89
  },
  {
    "tweeted_by": "ShapeShift 🦊",
    "@user": "ShapeShift_io",
    "tweet_time": "Tue May 05 17:20:54 +0000 2020",
    "tweet": "Do you want to win #BTC or #ETH in our next giveaway? \n🎁🎁🎁🎁🎁🎁🎁🎁🎁🎁🎁\n#bitcoin $BTC $ETH #crypto #CryptoGiveaway",
    "retweet_count": 36,
    "favorite_count": 68
  },
  {
    "tweeted_by": "Grayscale",
    "@user": "GrayscaleInvest",
    "tweet_time": "Tue May 05 21:01:10 +0000 2020",
    "tweet": "05/05/20 UPDATE: Net Assets Under Management, Holdings per Share, and Market Price per Share for our Investment Products.\n\nTotal AUM: $3.3 billion\n\n$BTC $BCH $ETH $ETC $ZEN $LTC $XLM $XRP $ZEC https://t.co/2ChuLGVEMn",
    "retweet_count": 10,
    "favorite_count": 24
  },
  {
    "tweeted_by": "Raoul Pal",
    "@user": "RaoulGMI",
    "tweet_time": "Tue May 05 23:54:09 +0000 2020",
    "tweet": "We are just mulling over an idea at @RealVision and wanted your input. Would you be interested in a RV Crytpo/Digital add-on membership tier where we purely focus on that space? Obviously, we would need to charge (in $ and crypto) for it as it means more production etc. $BTC",
    "retweet_count": 14,
    "favorite_count": 264
  },
  {
    "tweeted_by": "Crypto.com",
    "@user": "cryptocom",
    "tweet_time": "Thu Apr 30 07:00:20 +0000 2020",
    "tweet": "💡Quiz time🧠\n\nQ: You referred 5 friends to sign up for https://t.co/vCNztATkNg App, 3 of them got their metal cards, how much did you get?\n\n10 winners to share $1,000 USD in $BTC who:\n✅Follow\n✅Like\n✅Retweet w/ #CryptoComQuiz\n✅Answer below 👇 https://t.co/3yE2PM5QxG",
    "retweet_count": 1704,
    "favorite_count": 3788
  },
  {
    "tweeted_by": "Kraken Exchange",
    "@user": "krakenfx",
    "tweet_time": "Mon May 04 01:50:00 +0000 2020",
    "tweet": "Q: What do you make of $BTC's big March price decline? \n\n@danheld: \"#Bitcoin performed phenomenally well. It survived a global pandemic without any banks or pedigreed institutions to back-stop it.\"\n\nGet more insights in Dan's latest #halving Q&amp;A below 👇\n\nhttps://t.co/DbbhtMcrB8",
    "retweet_count": 24,
    "favorite_count": 72
  },
  {
    "tweeted_by": "Kraken Exchange",
    "@user": "krakenfx",
    "tweet_time": "Tue May 05 18:55:00 +0000 2020",
    "tweet": "Q: What was it like to see $BTC's price spike in 2013? \n\n@danheld: \"It was validation I wasn't crazy. If you believed in #Bitcoin then, you felt a little nuts. It was nice to feel this might be bigger.\"\n\nDon't miss Dan's talk w/ @APompliano, watch below👇\n\nhttps://t.co/lCKYQwU3uJ",
    "retweet_count": 7,
    "favorite_count": 38
  },
  {
    "tweeted_by": "Binance.US 🇺🇸"  ,
    "@user": "BinanceAmerica",
    "tweet_time": "Mon May 04 02:00:26 +0000 2020",
    "tweet": "If $BTC is Michael Jordan, $____ is Dennis Rodman.\n#LastDance https://t.co/r8ekKj9Q7H",
    "retweet_count": 18,
    "favorite_count": 57
  },
  {
    "tweeted_by": "Independent Reserve",
    "@user": "indepreserve",
    "tweet_time": "Tue May 05 22:33:06 +0000 2020",
    "tweet": "The perpetual growth cycle of #Bitcoin\n\n\",
    "retweet_count": 7,
    "favorite_count": 18
  }
]  
```


Parameter       | Type       | Description
----------------|------------|-------------
tweeted_by      | string     | Tweeted by user.
@user           | string     | Twitter handle.
tweet_time      | string     | Timestamp of tweet.
tweet           | string     | Message body.
retweet_count   | int        | Count of retweets.
favorite_count  | int        | Count of favorites.
