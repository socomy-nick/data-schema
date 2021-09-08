# Data Schema

## Table Of Contents
- [User Collection](#user-collection)
- [KOL Collection](#kol-collection)
- [Focuses And Styles Collections](#focuses-and-styles-collections)
- [Instagram Posts Collection](#instagram-posts-collection)
- [Instagram Frames Collection](#instagram-frames-collection)


## User Collection

All user contact information is fully verified. Email is verified using 4-digit verification code built by Socomy using Mailgun and Phone is verified using 4-digit verification supplied by Twilio service. 

### Shape

```
{
	"_id" : <ObjectId>,
	"name" : <string>,
	"phone" : <string>,
	"email" : <string>,
}
```

### Example

```
{
	"_id" : ObjectId('5d318fe0a7b6b9e88208a765'),
	"name" : 'John Smith',
	"phone" : '+621111111111',
	"email" : 'hello@gmail.com',
}
```

## KOL Collection

### Shape

```
{
  "_id" : <ObjectId>,
  "user_id" : <ObjectId>,
  "style_ids" : <array>,
  "focus_ids" : <array>,
  "city_id" : <ObjectId>,
  "fb" : {
    "fb_user_id" : <string>,
    "fb_page_id" : <string>,
  },
  "ig" : {
    "ig_business_id" : <string>,
    "name" : <string>,
    "username" : <string>,
    "followers_count" : <int>,
    "follower_demographics" : {
      "cities" : {
        "values" : <object>,
        "percents" : <object>,
        "urban" : <int>,
        "total" : <int>,
      },
      "countries" : {
        "values" : <object>,
        "percents" : <object>,
        "total" : <int>,
      },
      "gender_age" : {
        "male" : {
          "values" : {
            "13-17" : <int>,
            "18-24" : <int>,
            "25-34" : <int>,
            "35-44" : <int>,
            "45-54" : <int>,
            "55-64" : <int>,
            "65+" : <int>,
          },
          "percents" : {
            "13-17" : <int>,
            "18-24" : <int>,
            "25-34" : <int>,
            "35-44" : <int>,
            "45-54" : <int>,
            "55-64" : <int>,
            "65+" : <int>,
          },
          "percent" : <int>,
          "total" : <int>,
        },
        "female" : {
          "values" : {
            "13-17" : <int>,
            "18-24" : <int>,
            "25-34" : <int>,
            "35-44" : <int>,
            "45-54" : <int>,
            "55-64" : <int>,
            "65+" : <int>,
          },
          "percents" : {
            "13-17" : <int>,
            "18-24" : <int>,
            "25-34" : <int>,
            "35-44" : <int>,
            "45-54" : <int>,
            "55-64" : <int>,
            "65+" : <int>,
          },
          "percent" : <int>,
          "total" : <int>,
        },
        "average" : <int>,
        "total" : <int>,
      },
    }
  },
  "yt" : {
    "yt_channel_id" : <string>,
    "yt_playlist_id" : <string>,
    "name" : <string>,
    "username" : <string>,
    "subscribers_count" : <int>,
    "subscribers_demographics" : {
      "countries" : {
        "values" : <object>,
        "percents" : <object>,
        "total" : <int>,
      },
      "gender_age" : {
        "male" : {
          "values" : {
            "13-17" : <int>,
            "18-24" : <int>,
            "25-34" : <int>,
            "35-44" : <int>,
            "45-54" : <int>,
            "55-64" : <int>,
            "65+" : <int>,
          },
          "percents" : {
            "13-17" : <int>,
            "18-24" : <int>,
            "25-34" : <int>,
            "35-44" : <int>,
            "45-54" : <int>,
            "55-64" : <int>,
            "65+" : <int>,
          },
          "percent" : <int>,
          "total" : <int>,
        },
        "female" : {
          "values" : {
            "13-17" : <int>,
            "18-24" : <int>,
            "25-34" : <int>,
            "35-44" : <int>,
            "45-54" : <int>,
            "55-64" : <int>,
            "65+" : <int>,
          },
          "percents" : {
            "13-17" : <int>,
            "18-24" : <int>,
            "25-34" : <int>,
            "35-44" : <int>,
            "45-54" : <int>,
            "55-64" : <int>,
            "65+" : <int>,
          },
          "percent" : <int>,
          "total" : <int>,
        },
        "average" : <int>,
        "total" : <int>,
      },
    }
  },
}
```


## Focuses And Styles Collections

There is one collection for focuses (i.e. interest groups) and one collection for styles. 

### Focuses

```
[
  {
    '_id': ObjectId('5eb384dc80dc266f83c868f2'),
    'labels': {
      'en': 'Music', 
      'id': 'Musik'
    }
  },{
    '_id': ObjectId('5eb384dc80dc266f83c868eb'),
    'labels': {
      'en': 'Makeup', 
      'id': 'Makeup'
    }
  },{
    '_id': ObjectId('5eb384dc80dc266f83c868ef'),
    'labels': {
      'en': 'Fitness', 
      'id': 'Fitness'
    }
  },{
    '_id': ObjectId('5eb384dc80dc266f83c868f0'),
    'labels': {
      'en': 'Gaming', 
      'id': 'Gaming'
    }
  },{
    '_id': ObjectId('5eb384dd80dc266f83c868f5'),
    'labels': {
      'en': 'Photography', 
      'id': 'Fotografi'
    }
  },{
    '_id': ObjectId('5eb384dc80dc266f83c868f4'),
    'labels': {
      'en': 'Travel', 
      'id': 'Travel'
    }
  },{
    '_id': ObjectId('5eb384dc80dc266f83c868ec'),
    'labels': {
      'en': 'Fashion', 
      'id': 'Fashion'
    }
  },{
    '_id': ObjectId('5eb384dc80dc266f83c868f1'),
    'labels': {
      'en': 'Wedding', 
      'id': 'Wedding'
    }
  },{
    '_id': ObjectId('5eb384dc80dc266f83c868ee'),
    'labels': {
      'en': 'Health', 
      'id': 'Kesehatan'
    }
  },{
    '_id': ObjectId('5eb384dc80dc266f83c868f3'),
    'labels': {
      'en': 'Dancing', 
      'id': 'Dance/Tarian'
    }
  },{
    '_id': ObjectId('5eb384dc80dc266f83c868ed'),
    'labels': {
      'en': 'Family', 
      'id': 'Keluarga'
    }
  },{
    '_id': ObjectId('5eb384dc80dc266f83c868ea'),
    'labels': {
      'en': 'Skincare', 
      'id': 'Skincare'
    }
  },{
    '_id': ObjectId('5eb384dd80dc266f83c868f7'),
    'labels': {
      'en': 'Food', 
      'id': 'Makanan'
    }
  },{
    '_id': ObjectId('5eb384dd80dc266f83c868f6'),
    'labels': {
      'en': 'Gadget', 
      'id': 'Gadget'
    }
  }
]
```

### Styles

```
[
  {
    '_id': ObjectId('5eb384dc80dc266f83c868e5'),
    'labels': {
      'en': 'Cute', 
      'id': 'Cute'
    }
  },{
    '_id': ObjectId('5eb384db80dc266f83c868de'),
    'labels': {
      'en': 'Sporty', 
      'id': 'Sporty'
    }
  },{
    '_id': ObjectId('5eb384dc80dc266f83c868e8'),
    'labels': {
      'en': 'Relatable', 
      'id': 'Standar/Relatable'
    }
  },{
    '_id': ObjectId('5eb384dc80dc266f83c868e2'),
    'labels': {
      'en': 'Mum / Home Maker', 
      'id': 'Ibu / Ibu Rumah Tangga'
    }
  },{
    '_id': ObjectId('5eb384dc80dc266f83c868e4'),
    'labels': {
      'en': 'Plus Size', 
      'id': 'Plus Size / Ukuran besar'
    }
  },{
    '_id': ObjectId('5eb384db80dc266f83c868df'),
    'labels': {
      'en': 'Elegant', 
      'id': 'Elegan'
    }
  },{
    '_id': ObjectId('5eb384db80dc266f83c868e0'),
    'labels': {
      'en': 'Sweet', 
      'id': 'Sweet'
    }
  },{
    '_id': ObjectId('5eb384db80dc266f83c868e1'),
    'labels': {
      'en': 'Artsy / Character Make Up',
      'id': 'Artsy / Make Up Karakter'
    }
  },{
    '_id': ObjectId('5eb384dc80dc266f83c868e3'),
    'labels': {
      'en': 'Make Up Artist', 
      'id': 'Make Up Artist'
    }
  },{
    '_id': ObjectId('5eb384dc80dc266f83c868e6'),
    'labels': {
      'en': 'Street Fashion', 
      'id': 'Street Fashion'
    }
  },{
    '_id': ObjectId('5eb384dc80dc266f83c868e9'),
    'labels': {
      'en': 'Edgy', 
      'id': 'Edgy'
    }
  },{
    '_id': ObjectId('5eb384dc80dc266f83c868e7'),
    'labels': {
      'en': 'Casual', 
      'id': 'Kasual'
    }
  }
]
```





## Instagram Posts Collection




## Instagram Frames Collection

Data related to the instagram frames created by each KOL 

### Shape

Note, for instagram frames, likes and comments will always have a value of 0 since users can't like/comment on them. Also, note that captions were only added to the API around end of 2020 / early 2021 which means earlier frames will have a blank value for captions. 

```
{
	"_id" : <ObjectId>,
	"kol_id" : <ObjectId>,
	"ig_media_id" : <string>,
	"ig_business_id" : <string>,
	"caption" : <string>,
	"comments_count" : <int>,
	"like_count" : <int>,
	"media_type" : <string>,
	"permalink" : <string>,
	"published_at" : <Date>,
	"insights" : {
		"reach" : <int>,
		"impressions" : <int>,
		"taps_forward" : <int>,
		"taps_back" : <int>,
		"exits" : <int>,
		"replies" : <int>
	}
}
```
  
### Example

```
{
	"_id" : ObjectId('5dcd07e520c79c4bfd4997d7'),
	"ig_media_id" : '18115231966042755',
	"ig_business_id" : '17841401226613021',
	"caption" : '',
	"comments_count" : 0,
	"like_count" : 0,
	"media_type" : 'VIDEO',
	"permalink" : 'https://instagram.com/stories/kintanptrrr/2176812014711014571',
	"published_at" : datetime.datetime(2019, 11, 14, 7, 23, 54),
	"insights" : {
		"reach" : 1713,
		"impressions" : 2544,
		"taps_forward" : 1521,
		"taps_back" : 443,
		"exits" : 79,
		"replies" : 21,
	}
}
```


