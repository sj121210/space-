space-
======

i have a calculator project which required to build cal GUI on wxfb first then executed by spyder , but my code couldn't do any functions on the cal can sb help? thanks
"""
Created on Fri Sep 21 

@author: jsj1992
"""

import sys
sys.path.append("/usr/local/lib/wxPython-3.0.0.0/lib/python2.7/site-packages/wx-3.0-osx_cocoa")
import wx
import gui

# Implementing MainFrame
class CalcMainFrame( gui.MainFrame ):
	def __init__( self, parent ):
		gui.MainFrame.__init__( self, parent )
	
 
def m_button1Function (self,event):
        try:
            t1=float(self.m_textCtrl1.value)
            t2=float(self.m_textCtrl2.value)
            self.m_textCtrl3.Setvalue(str(t1+t2))
        except:
            msgStr = 'Bad input\nPlease try again'
            wx.MessageBox(msgStr)
def m_button2Function (self,event):
        try:
            t1=float(self.m_textCtrl1.value)
            t2=float(self.m_textCtrl2.value)
            self.m_textCtrl3.Setvalue(str(t1-t2))
        except:
            msgStr='Bad input\nPlease try again'
            wx.MessageBox(msgStr)
        
def m_button3Function (self,event):
        try:
            t1=float(self.text.GetValue())
            t2=float(self.text.GetValue())
            self.text.Setvalue(str(t1*t2))
        except:
            msgStr='Bad input\nPlease try again'
            wx.MessageBox(msgStr)
    
def m_button4Function (self,event):
        try:
            t1=float(self.m_textCtrl1.value)
            t2=float(self.m_textCtrl2.value)
            self.m_textCtrl3.Setvalue(str(t1/t2))
        except:
            msgStr='Bad input\nPlease try again'
            wx.MessageBox(msgStr)
            
def m_button5Function(self,event):
        self.m_textCtrl1.SetValue('')
        self.m_textCtrl2.SetValue('')
        self.m_textCtrl3.SetValue('')
        
myApp = wx.App(False)
myFrame =gui.MainFrame(None)
myFrame.Show(True)
myApp.MainLoop()
