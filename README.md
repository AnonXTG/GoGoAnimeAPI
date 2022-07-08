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
                            
