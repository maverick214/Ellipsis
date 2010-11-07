import xbmc, xbmcgui, urllib

news = urllib.urlopen("http://www.teamblackbolt.co.uk/EllipsisNews.php")
newstext = news.read()

if (not newstext.startswith('[TBBNEWS]')):
	newstext = 'Unable to fetch date from server. Please check your connection and try again later.'
else:
	newstext = newstext.replace('[TBBNEWS]', '')
	
xbmcgui.Window(10000).setProperty("TeamBlackbolt.News",newstext)
