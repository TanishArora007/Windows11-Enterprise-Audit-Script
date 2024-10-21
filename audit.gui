import os
import subprocess
import customtkinter as ctk

class AuditToolGUI:
    def __init__(self, master):
        self.master = master
        master.title("CIS Benchmark Audit Tool")
        master.geometry("1000x700")
        
        ctk.set_appearance_mode("Dark")
        ctk.set_default_color_theme("blue")
        
        self.create_widgets()
        
    def create_widgets(self):
        
        start_icon_path = "start_icon.png"
        export_icon_path = "export_icon.png"
        clean_icon_path = "clean_icon.png"

        self.start_icon = ctk.CTkImage(file=start_icon_path) if os.path.exists(start_icon_path) else None
        self.export_icon = ctk.CTkImage(file=export_icon_path) if os.path.exists(export_icon_path) else None
        self.clean_icon = ctk.CTkImage(file=clean_icon_path) if os.path.exists(clean_icon_path) else None

        # Main frame
        main_frame = ctk.CTkFrame(self.master, corner_radius=15, fg_color="#2b2b2b")
        main_frame.pack(fill="both", expand=True, padx=20, pady=20)
        
        # Title
        title_label = ctk.CTkLabel(main_frame, text="CIS Benchmark Audit Tool", 
                                   font=ctk.CTkFont(size=28, weight="bold"), text_color="#eaeaea")
        title_label.pack(pady=(20, 10))
        
        # OS Selection Frame
        os_frame = ctk.CTkFrame(main_frame, fg_color="#3a3a3a", corner_radius=10)
        os_frame.pack(fill="x", pady=20, padx=20)
        
        os_label = ctk.CTkLabel(os_frame, text="Selected Operating System: Ubuntu/Windows 11 Audit Generator", 
                                font=ctk.CTkFont(size=18, weight="bold"), text_color="#cccccc")
        os_label.pack(side="left", padx=(10, 20), pady=10)
        
        # Start Audit Button
        start_button = ctk.CTkButton(main_frame, text=" Start Audit", 
                                     command=self.start_audit, image=self.start_icon, compound="left",
                                     font=ctk.CTkFont(size=16, weight="bold"), corner_radius=10,
                                     hover=True, hover_color="#1a8cff")
        start_button.pack(pady=20)
        
        # Results Frame
        results_frame = ctk.CTkFrame(main_frame)
        results_frame.pack(fill="both", expand=True, pady=10, padx=20)
        
        # Passed Audits
        passed_frame = ctk.CTkFrame(results_frame, fg_color="#3a3a3a", corner_radius=10)
        passed_frame.pack(side="left", fill="both", expand=True, padx=10)
        
        passed_label = ctk.CTkLabel(passed_frame, text="Working Audits (Passed):", 
                                    font=ctk.CTkFont(size=16, weight="bold"), text_color="#b2ff59")
        passed_label.pack(pady=10)
        
        self.passed_text = ctk.CTkTextbox(passed_frame, wrap="word", 
                                          font=ctk.CTkFont(size=14), fg_color="#2b2b2b", text_color="#ffffff", corner_radius=10)
        self.passed_text.pack(fill="both", expand=True, padx=10, pady=10)
        
        # Failed Audits
        failed_frame = ctk.CTkFrame(results_frame, fg_color="#3a3a3a", corner_radius=10)
        failed_frame.pack(side="right", fill="both", expand=True, padx=10)
        
        failed_label = ctk.CTkLabel(failed_frame, text="Failed Audits:", 
                                    font=ctk.CTkFont(size=16, weight="bold"), text_color="#ff5252")
        failed_label.pack(pady=10)
        
        self.failed_text = ctk.CTkTextbox(failed_frame, wrap="word", 
                                          font=ctk.CTkFont(size=14), fg_color="#2b2b2b", text_color="#ffffff", corner_radius=10)
        self.failed_text.pack(fill="both", expand=True, padx=10, pady=10)
        
        # Button Frame
        button_frame = ctk.CTkFrame(main_frame, fg_color="transparent")
        button_frame.pack(fill="x", pady=20)
        
        # Center-align buttons
        button_frame.columnconfigure(0, weight=1)
        button_frame.columnconfigure(3, weight=1)
        
        # Export Button
        export
