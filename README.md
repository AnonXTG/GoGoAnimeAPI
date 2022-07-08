# GoGoAnimeAPI

An unofficial **cloned** gogoanime api Library for Python where you can get free Dubbed and Subbed Download Links of almost all Anime.
The Default Dubbed anime Language is English.

## Installation
```$ pip3 install gogoanime-api```

## Usage
### 1. Importing the Library
```from gogoanimeapi import gogoanime as anime```
### 2. Searching Anime by Manual Input
```anime_search = anime.get_search_results(query="Tonikaku Kawaii")```
###
#### This will return a list of dictionaries containing Anime "name" and "animeid":
```
[{'name': 'Tonikaku Kawaii', 'animeid': 'tonikaku-kawaii'}, 
        {'name': 'Tonikaku Kawaii OVA', 'animeid': 'tonikaku-kawaii-ova'}, 
            {'name': 'Tonikaku Kawaii (Dub)', 'animeid': 'tonikaku-kawaii-dub'}]
```
###
#### Getting the name of anime search results:
```
for title in anime_search:
    print(title.get('name'))
```
###
#### This will print the following:
```
Tonikaku Kawaii
Tonikaku Kawaii OVA
Tonikaku Kawaii (Dub)
```
Likewise, You can get "animeid" by this method.
### 3. Getting Anime Details by animeid:
```anime_details = anime.get_anime_details(animeid="tonikaku-kawaii-dub")```
###
#### This will return a dictionary containing the Detials of Anime of animeid:
```
{'title': 'Tonikaku Kawaii (Dub)', 
    
    'year': '2020', 
    
        'other_names': 'Other name: TONIKAWA: Over the Moon For You, Generally Cute, Fly Me to the Moon, Generally Cute, Fly Me to the Moon', 
        
            'type': 'Fall 2020 Anime', 
            
                'status': 'Completed', 
                
                    'genre': "['Comedy', 'Romance', 'Shounen']", 
                    
                        'episodes': '12', 
                        
                            'image_url': 'https://gogocdn.net/cover/tonikaku-kawaii-dub.png', 
              

'plot_summary': " Having grown up ridiculed for his bizarre name, Nasa Yuzaki strives to be remembered for something more. Fortunately, it seems he's on the right path, ranking first in the nation's mock exams and set to enter his high school of choice.\r\n\r\nHowever, everything changes in a single night when he notices a girl across the street on his way home. Enraptured by her overwhelming cuteness, it's love at first sight for Nasa. But in his infatuated daze, he fails to notice the approaching danger speeding down the road and finds himself at death's door. Barely alive thanks to the girl's intervention, Nasa musters the courage to confess his love to her, fearing she might otherwise vanish from his life. She accepts his proposal on one condition marriage, to which Nasa gladly accepts before passing out from his injuries. Upon waking, however, the girl is nowhere to be found.\r\n\r\nAfter recovering from his injuries, Nasa tosses his previous ambitions aside and dedicates his life to finding the girl that captured his heart, yet several years pass to no avail. But one night, when an unexpected visitor comes knocking on his door, Nasa finds himself facing a woman that would forever change his world his wife."
                                 }
```
###
#### Getting a Specific detail of Anime:
```
released_year = anime_details.get('year')
println(released_year)
```
#### This will return the released year of Anime:
```2020```

Likewise, You can get any details mentioned above for your app.

### 4. Getting Download Links for an Anime:
```anime_link = anime.get_episodes_link(animeid="tonikaku-kawaii-dub", episode_num=3)```
###
#### This will return a dictionary of all Available Download Links:
```
{
'title': 'Tonikaku Kawaii (Dub)', 
    
    '(HDP-mp4)': 'https://storage.googleapis.com/crucial-accord-306602/CA_K18ZXRJO/23a_1616976498148615.mp4', 
        
        '(360P-mp4)': 'https://cdn11.cloud9xx.com/user1342/71bf4a5b831f51fedfa37a92d297b153/EP.3.360p.mp4?token=N-YGTQyVtMUODT9DhbS_mA&expires=1617107204&id=148615', 
      
'(720P-mp4)': 'https://cdn11.cloud9xx.com/user1342/71bf4a5b831f51fedfa37a92d297b153/EP.3.720p.mp4?token=yUGXZW6qloVIekqqgaoGrw&expires=1617107204&id=148615', 
        
   '(1080P-mp4)': 'https://cdn11.cloud9xx.com/user1342/71bf4a5b831f51fedfa37a92d297b153/EP.3.1080p.mp4?token=72r_zWsyDbuVeRtfkSPv4g&expires=1617107204&id=148615', 
      
'StreamSB': 'https://streamsb.net/d/xf1j1hoaz5c2.html', 
                        
                        'StreamTape': 'https://streamtape.com/v/yV1vLdYe3MF18Xe/tonikaku-kawaii-dub-episode-3.mp4', 
                                                                     
