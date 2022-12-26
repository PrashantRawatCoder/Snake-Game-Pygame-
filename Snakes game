'''Created by : Prashant Rawat
   DATE : 14/05/2021
   Idea : CodeWithHarry
   class : 7th B
   
   
   
   Wish : maby a laptop for more coding/programming contant .
   THANK YOU FOR VISITING MY PROGRAMMING FILE
    '''




import pygame
from pygame.locals import *
import random
import sys

def skl(gw,cl,sk):
		pygame.draw.rect(gw,cl,sk)
sn_l=1
sn_lis=[]
	

class main():
	
	pygame.init()
	screen= pygame.display.set_mode((1,1))
	pygame.display.set_caption("Snake Game")
	re1=pygame.Rect(145,1120,150,150)
	re2=pygame.Rect(455,1120,150,150)
	re3=pygame.Rect(300,1080,150,150)
	re4=pygame.Rect(300,1240,150,150)
	bo1=pygame.Rect(5,5,710,5)
	bo2=pygame.Rect(5,1050,710,5)
	bo3=pygame.Rect(710,5,5,1050)
	bo4=pygame.Rect(5,5,5,1050)
	point=0
	
	sx=20
	sy=20
	vlx=0
	vly=0
	fx=random.randint(40,680)
	fy=random.randint(40,1020)
	ptext="Pause"
	run=True
	gameover=False
	try :
		with open("high_score.txt","r") as j:
			pass
	except :
		with open("high_score.txt","w") as j:
			j.write("0")
	try :
		with open("snle.txt","r") as j:
			pass
	except :
		with open("snle.txt","w") as j:
			j.write("noob")
	while run:
		if gameover:
			with open("high_score.txt","r") as hisc:
				h_s=hisc.read()
				if int(h_s)<point:
					with open("high_score.txt","r+") as dhs:
						dhs.write(str(point))
				
			
			rep=pygame.Rect(100,200,230,70)
			exit=pygame.Rect(350,200,230,70)
			hsc=pygame.Rect(220,400,295,70)
			lev=pygame.Rect(247,500,230,70)
			screen.fill((100,30,250))
			pygame.draw.rect(screen,[200,0,0],rep)
			pygame.draw.rect(screen,[200,0,0],exit)
			pygame.draw.rect(screen,[200,0,0],hsc)
			pygame.draw.rect(screen,[200,0,0],lev)
			
			fon=pygame.font.SysFont('Arial', 60)
			sf=pygame.font.SysFont('Arial', 100)
			screen.blit(sf.render('Game Over', True, (255,55,25)), (95, 50))
			
			screen.blit(fon.render('Replay', True, (0,205,20)), (102, 202))
			screen.blit(fon.render('Exit', True, (0,205,20)), (352, 202))
			screen.blit(fon.render('High Score', True, (0,205,20)), (222,402))
			screen.blit(fon.render('Level', True, (0,205,20)), (259,504))
			screen.blit(sf.render('Score : '+str(point), True, (255,136,43)), (175,600))
			
			for event in pygame.event.get():
				if event.type == pygame.QUIT:
					run=False
				if event.type == pygame.MOUSEBUTTONDOWN:
					mouse_p=event.pos
					
					if exit.collidepoint(mouse_p):
						run=False
					elif rep.collidepoint(mouse_p):
						point=0
	
						sx=20
						sy=20
						vlx=0
						vly=0
						fx=random.randint(40,690)
						fy=random.randint(40,1030)
						run=True
						gameover=False
						sn_l=1
						sn_lis=[]
					elif hsc.collidepoint(mouse_p):
						
						hrun=True
						while hrun:
							
							screen.fill((100,30,250))
							Back=pygame.Rect(247,600,200,70)
							reset=pygame.Rect(247,700,200,70)
							pygame.draw.rect(screen,[200,0,0],Back)
							pygame.draw.rect(screen,[200,0,0],reset)
							screen.blit(fon.render('High Score : '+h_s, True, (0,205,20)), (212,402))
							screen.blit(fon.render('Back', True, (0,205,20)), (249, 602))
							screen.blit(fon.render('Reset', True, (0,205,20)), (249, 702))
							
							pygame.display.update()
							for event in pygame.event.get():
								if event.type == pygame.QUIT:
									run=False
								if event.type == pygame.MOUSEBUTTONDOWN:
									m_p=event.pos
									if Back.collidepoint(m_p):
										hrun=False
									elif reset.collidepoint(m_p):
										with open("high_score.txt","w") as dhs:
											dhs.write("0")
			
					elif lev.collidepoint(mouse_p):
						hrun=True
						with open("snle.txt","r") as leclor:
							ifle=leclor.read()
						if ifle=="noob":
							leco=[[200,100,100],[200,0,0],[200,0,0]]
						elif ifle=="pro":
							leco=[[200,0,0],[200,100,100],[200,0,0]]
						elif ifle=="god":
							leco=[[200,0,0],[200,0,0],[200,100,100]]
						while hrun:
											
							screen.fill((100,30,250))
							Back=pygame.Rect(247,900,200,70)
							noob=pygame.Rect(210,400,200,70)
							pro=pygame.Rect(210,500,200,70)
							god=pygame.Rect(210,600,200,70)
							
							for event in pygame.event.get():
								if event.type == pygame.QUIT:
									run=False
								if event.type == pygame.MOUSEBUTTONDOWN:
									m_p=event.pos
									if Back.collidepoint(m_p):
										hrun=False
									elif noob.collidepoint(m_p):
										with open("snle.txt","w") as le:
											le.write("noob")
										leco=[[200,100,100],[200,0,0],[200,0,0]]
									elif pro.collidepoint(m_p):
										with open("snle.txt","w") as le:
											le.write("pro")
										leco=[[200,0,0],[200,100,100],[200,0,0]]
									elif god.collidepoint(m_p):
										with open("snle.txt","w") as le:
											le.write("god")
										leco=[[200,0,0],[200,0,0],[200,100,100]]
							pygame.draw.rect(screen,[200,0,0],Back)
							pygame.draw.rect(screen,leco[0],noob)
							pygame.draw.rect(screen,leco[1],pro)
							pygame.draw.rect(screen,leco[2],god)
							
							screen.blit(fon.render('Noob', True, (0,205,20)), (212,402))
							screen.blit(fon.render('Pro', True, (0,205,20)), (212,502))
							screen.blit(fon.render('God', True, (0,205,20)), (212,602))
							screen.blit(fon.render('Back', True, (0,205,20)), (249, 902))
											
							pygame.display.update()
					
					


			pygame.display.update()
							
							
							
			
							
											
															
																			
				
																											
																																																		
																																																																																																
		elif not gameover :
			for event in pygame.event.get():
				if event.type == pygame.QUIT:
					run=False
				if event.type == pygame.MOUSEBUTTONDOWN:
					mouse_p=event.pos
					with open("snle.txt","r") as le:
						adle=le.read()
						if adle=="noob":
							add_lev=3
						elif adle=="pro":
							add_lev=5
						elif adle=="god":
							add_lev=7
					if re1.collidepoint(mouse_p):
	
						
						vlx=-add_lev
						vly=0
					elif re2.collidepoint(mouse_p):
	
						vlx=add_lev
						vly=0
						
						
					elif re3.collidepoint(mouse_p):
						
						vly=-add_lev
						vlx=0
						
					elif re4.collidepoint(mouse_p):
					
							
						vly=add_lev
						vlx=0
					elif paus.collidepoint(mouse_p):
						hrun=True
						while hrun:
							
							ptext="Continue"
							paus=pygame.Rect(455,1285,260,70)
							pygame.draw.rect(screen,[255,0,0],paus)
							screen.blit(font.render(ptext, True, (255,255,255)), (457, 1287))
							quit=pygame.Rect(5,1285,260,70)
							pygame.draw.rect(screen,[255,0,0],quit)
							screen.blit(font.render("Quit", True, (255,255,255)), (5, 1287))
							
							pygame.display.update()
							for event in pygame.event.get():
								if event.type == pygame.QUIT:
									run=False
								if event.type == pygame.MOUSEBUTTONDOWN:
									mouse_p=event.pos
								
									if paus.collidepoint(mouse_p):
										ptext="Pause"
										hrun=False
									elif quit.collidepoint(mouse_p):
										gameover=True
										hrun=False
					
						
			sx+=vlx
			sy+=vly
			
					
			screen.fill((100,100,255))
			#boundries
			pygame.draw.rect(screen,[200,0,0],bo1)
			pygame.draw.rect(screen,[200,0,0],bo2)
			pygame.draw.rect(screen,[200,0,0],bo3)
			pygame.draw.rect(screen,[200,0,0],bo4)
			#pause button
			paus=pygame.Rect(455,1285,260,70)
			pygame.draw.rect(screen,[255,0,0],paus)
			#buttons
			pygame.draw.rect(screen,[0,0,0],re1)
			pygame.draw.rect(screen,[0,0,0],re2)
			pygame.draw.rect(screen,[0,0,0],re3)
			pygame.draw.rect(screen,[0,0,0],re4)
			#text on buttons
			font=pygame.font.SysFont('Arial', 40)
			screen.blit(font.render('⟨ ⟨', True, (255,255,255)), (200, 1170))
			screen.blit(font.render('⟩ ⟩', True, (255,255,255)), (530, 1170))
			screen.blit(font.render('/\ ', True, (255,255,255)), (350, 1110))
			screen.blit(font.render('\/ ', True, (255,255,255)), (350, 1280))
			screen.blit(font.render(ptext, True, (255,255,255)), (457, 1287))
			
			#score
			screen.blit(font.render("Score : "+str(point), True, (255,5,5)), (10, 1060))
			
			#food
			ap=pygame.Rect(fx,fy,30,30)
			
			he=[]
			he.append(sx)
			he.append(sy)
			sn_lis.append(he)
			head=pygame.Rect(sx,sy,35,35)
	
			hj=True
			num=0
			for x,y in sn_lis:
				
				if hj:
					rect=pygame.Rect(x,y,35,35)
					skl(screen,[255,100,100],rect)
					hj=False
				else:
					rect=pygame.Rect(x,y,35,35)
					skl(screen,[30,150,30],rect)
					hj=True
				num+=1
				if len(sn_lis)>sn_l:
					del sn_lis[0]
			
			#if food_x or food_y change tis change becuase this is draw every time when loop is running again
			pygame.draw.rect(screen,(150,10,10),ap)
			if head.colliderect(ap):
				point+=1
				fx=random.randint(40,680)
				fy=random.randint(40,1020)
				sn_l+=20
					
			
			
			#check if snake is not colliding to boundries 
			# it is here because if it is in events loop it has touch boundries 2 times
			if head.colliderect(bo1) or head.colliderect(bo2) or head.colliderect(bo3) or head.colliderect(bo4):
				gameover=True
			
			elif he in sn_lis[:-1] :
				gameover=True
			
			pygame.display.update()
	pygame.quit()
	sys.exit
			
	

if __name__=="__main__":
	main()
			
