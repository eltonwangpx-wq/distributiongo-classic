# DistributionGo Classic 2.2.0

[繁體中文](#繁體中文) · [简体中文](#简体中文) · [English](#english) · [日本語](#日本語) · [ไทย](#ไทย) · [Tiếng Việt](#tiếng-việt) · [Bahasa Indonesia](#bahasa-indonesia) · [한국어](#한국어) · [Español](#español)

## 繁體中文

1. 需要 Windows 11 x64 24H2 以上、管理員權限及至少 5 GiB 可用磁碟空間；升級另需足夠空間保存資料與舊程式。只需下載 Setup EXE，核對同版 SHA-256 後執行。此版未做程式碼簽章，Windows 可能提示未知發行者；請確認下載來源。
2. 選完整安裝，或依部署需求選僅資料庫／僅 Web。Web-only 須匯入 DB 主機提供的受保護連線檔。安裝程式不安裝 Odoo Server；Odoo 選項只供既有本機 Odoo 19 使用。
3. 選擇本機 IP／主機名稱及允許來源。`LocalSubnet` 表示本機子網，亦可指定 IPv4 CIDR；規則適用所有 Windows 網路類別，不代表開放所有來源。測試環境安裝約 5～10 分鐘，請查看步驟與已等待時間。
4. 完成後從桌面／開始功能表的 DistributionGo Web 開啟。新裝帳密 `admin / distributiongo`；建議登入後立即改密碼。預設倉庫 `0000 / default`，admin 已是成員。永久資訊為程式目錄內 `InstallationInfo.txt`，不含密碼。
5. 純區網使用內部 CA：在「憑證信任與匯出」核對 SHA-256 指紋，管理員明確確認後設定本機信任。其他電腦需匯出 ZIP 並各設定一次。請勿把略過瀏覽器警告當作正式設定。正式網域可匯入涵蓋該名稱的 PFX；Let’s Encrypt 可免費簽發網域憑證，但本版不自動申請／續期，須由管理員管理並重新匯入。
6. 再執行 Setup 可選修改設定、升級或接回保留資料。移除程式保留資料目錄；不要為更新刪除它。備份／還原詳見 [維運說明](../README.md#backup-and-recovery-administrator-powershell)，適用相同主機、角色、路徑與應用包，含私鑰，請勿公開。Web-only 的遠端 DB 必須另外備份。
7. ThousanAI 入口預設啟用，每台主機產生獨立金鑰，不內附模型 API Key。雲端功能需要網路與既有隱私告知同意；未提問時不會因安裝自動送出問題。

## 简体中文

需要 Windows 11 x64 24H2 以上、管理员权限和至少 5 GiB 可用空间；升级还需保存数据及旧程序的空间。只下载 Setup EXE，核对 SHA-256。此版未签名，Windows 可能提示未知发布者，请确认来源。选择完整安装、仅数据库或仅 Web；Web-only 需要 DB 主机的受保护连接文件。不安装 Odoo Server，附加组件只用于已有本机 Odoo 19。

选择本机 IP／主机名与允许来源；`LocalSubnet` 表示本机子网，也可填 IPv4 CIDR。规则适用所有 Windows 网络类型，但仍限制来源。测试安装约 5～10 分钟，可查看步骤及等待时间。完成后使用桌面或开始菜单 Web 快捷方式。新装账号 `admin / distributiongo`，请修改密码；默认仓库 `0000 / default`，admin 已加入。程序目录的 `InstallationInfo.txt` 保存网址、DB 地址／端口与允许来源，不含密码。

局域网 HTTPS 需在“证书信任与导出”核对指纹并由管理员确认信任；其他电脑导入导出的 ZIP 各设置一次。正式域名可导入 PFX；Let’s Encrypt 证书免费，但申请与续期需管理员负责，本版不自动办理。不要把跳过警告当作正式配置。

再次执行 Setup 可修改、升级或接回保留数据。卸载保留数据目录，请勿为更新删除它。[备份与还原](../README.md#backup-and-recovery-administrator-powershell)要求相同主机、角色、路径与应用包；备份含私钥，不可公开。Web-only 的远程 DB 另备份。ThousanAI 默认启用入口，主机独立密钥、不附模型 API Key；云端提问需要网络与隐私同意。

## English

Requires Windows 11 x64 24H2 or later, administrator approval, and at least 5 GiB free. Updates need additional room for the database and previous application. Download only Setup EXE and verify its release SHA-256. This release is unsigned: Windows may show an unknown-publisher warning; verify the download source.

Choose Full, Database-only or Web-only. Web-only imports a protected connection file from its database host. Setup does not install Odoo Server; the optional connector targets an existing local Odoo 19. Select a local address and allowed source range. `LocalSubnet` or an IPv4 CIDR restricts clients on all Windows network profiles. Installation took about 5–10 minutes in testing; follow the displayed steps and elapsed time.

Open DistributionGo Web from the desktop or Start menu. New installation: `admin / distributiongo`; change the password after signing in. Warehouse `0000 / default` includes admin. `InstallationInfo.txt` in the program directory records endpoints and allowed sources without passwords.

For LAN HTTPS, open Certificate trust and export, verify the fingerprint, and explicitly approve local trust as administrator. Export a ZIP for each other client to configure once. Do not rely on bypassing browser warnings. For a formal domain, import a matching PFX. Let’s Encrypt certificates are free, but issuance, renewal and reimport are administrator-managed; this installer does not automate them.

Run Setup again to modify settings, upgrade or reinstall using retained data. Uninstall keeps the data directory. [Backup and recovery](../README.md#backup-and-recovery-administrator-powershell) require the same host, role, paths and application package. Backups contain private keys: keep them protected. A Web-only backup does not include the remote database. ThousanAI starts enabled with a unique local key, without a bundled model API key; cloud questions require connectivity and privacy consent.

## 日本語

Windows 11 x64 24H2 以降、管理者権限、5 GiB 以上の空き容量が必要です。更新時はデータと旧プログラムの保存容量も必要です。Setup EXE のみをダウンロードし、SHA-256 を確認してください。未署名のため、不明な発行元の警告が出る場合があります。

完全／データベースのみ／Web のみを選択します。Web のみでは DB ホストの保護された接続ファイルが必要です。Odoo Server はインストールせず、コネクターは既存のローカル Odoo 19 用です。ローカル IP と許可元を選択します。`LocalSubnet` または IPv4 CIDR の制限はすべての Windows ネットワーク種別に適用されます。テストでは約 5～10 分かかります。

デスクトップまたはスタートメニューから Web を開きます。初期アカウントは `admin / distributiongo`、倉庫は `0000 / default` で admin が所属します。ログイン後にパスワードを変更してください。接続情報はプログラムフォルダーの `InstallationInfo.txt` に保存され、パスワードは含みません。

LAN 証明書は「信頼とエクスポート」で指紋を照合し、管理者が明示的に信頼を設定します。他の PC には ZIP を渡して一度設定します。正式ドメインは対応する PFX を使用できます。Let’s Encrypt は無料ですが、発行・更新・再インポートは管理者が行います。警告の回避を通常運用にしないでください。

Setup から設定変更、更新、保持データでの再インストールができます。アンインストールしてもデータは保持されます。[バックアップと復元](../README.md#backup-and-recovery-administrator-powershell)は同じホスト、役割、パス、アプリケーションパッケージ用です。秘密鍵を含むため公開しないでください。リモート DB は別途バックアップします。ThousanAI はホスト固有鍵で有効になり、モデル API キーは付属しません。クラウドへの質問にはネット接続とプライバシー同意が必要です。

## ไทย

ต้องใช้ Windows 11 x64 24H2 ขึ้นไป สิทธิ์ผู้ดูแลระบบ และพื้นที่ว่างอย่างน้อย 5 GiB การอัปเกรดต้องมีพื้นที่สำหรับข้อมูลและโปรแกรมเดิม ดาวน์โหลดเฉพาะ Setup EXE และตรวจ SHA-256 รุ่นนี้ยังไม่ลงลายเซ็น Windows อาจแจ้งผู้เผยแพร่ที่ไม่รู้จัก

เลือกติดตั้งครบชุด เฉพาะฐานข้อมูล หรือเฉพาะ Web โดย Web-only ต้องใช้ไฟล์เชื่อมต่อที่ป้องกันจากเครื่อง DB ไม่ติดตั้ง Odoo Server ตัวเชื่อมต่อใช้กับ Odoo 19 ที่มีอยู่ในเครื่อง เลือก IP และแหล่งที่อนุญาต `LocalSubnet` หรือ IPv4 CIDR จะจำกัดไคลเอนต์ในทุกประเภทเครือข่าย Windows เวลาทดสอบประมาณ 5–10 นาที ดูขั้นตอนและเวลาที่ผ่านไป

เปิด DistributionGo Web จากเดสก์ท็อปหรือ Start บัญชีใหม่คือ `admin / distributiongo` ควรเปลี่ยนรหัสผ่าน คลัง `0000 / default` มี admin เป็นสมาชิก ข้อมูล URL และ DB อยู่ใน `InstallationInfo.txt` ในโฟลเดอร์โปรแกรมโดยไม่มีรหัสผ่าน

สำหรับ LAN ให้ตรวจลายนิ้วมือในเครื่องมือความเชื่อถือใบรับรองและยืนยันด้วยผู้ดูแลระบบ ส่งออก ZIP เพื่อตั้งค่าคอมพิวเตอร์อื่นครั้งเดียว โดเมนจริงใช้ PFX ที่ตรงกันได้ Let’s Encrypt ฟรี แต่ผู้ดูแลต้องออก ต่ออายุ และนำเข้าเอง ไม่ควรใช้การข้ามคำเตือนเป็นการตั้งค่าถาวร

เปิด Setup อีกครั้งเพื่อแก้ไข อัปเกรด หรือติดตั้งใหม่ด้วยข้อมูลเดิม การถอนติดตั้งเก็บข้อมูลไว้ [การสำรองและกู้คืน](../README.md#backup-and-recovery-administrator-powershell)ใช้กับเครื่อง บทบาท พาธ และแพ็กเกจเดิมเท่านั้น มีคีย์ส่วนตัวจึงห้ามเผยแพร่ DB ระยะไกลต้องสำรองแยก ThousanAI เปิดทางเข้าโดยใช้คีย์เฉพาะเครื่อง ไม่แถม API Key ของโมเดล การถามบนคลาวด์ต้องมีอินเทอร์เน็ตและยอมรับความเป็นส่วนตัว

## Tiếng Việt

Cần Windows 11 x64 24H2 trở lên, quyền quản trị và ít nhất 5 GiB trống; nâng cấp cần thêm chỗ cho dữ liệu và chương trình cũ. Chỉ tải Setup EXE và kiểm tra SHA-256. Bản này chưa ký số nên Windows có thể báo nhà phát hành không xác định.

Chọn đầy đủ, chỉ cơ sở dữ liệu hoặc chỉ Web. Web-only cần tệp kết nối được bảo vệ từ máy DB. Không cài Odoo Server; trình kết nối dành cho Odoo 19 đã có trên máy. Chọn IP cục bộ và nguồn cho phép. `LocalSubnet` hoặc IPv4 CIDR giới hạn máy khách trên mọi loại mạng Windows. Thời gian thử nghiệm khoảng 5–10 phút; xem các bước và thời gian đã chờ.

Mở Web từ màn hình nền hoặc Start. Tài khoản mới `admin / distributiongo`, nên đổi mật khẩu. Kho `0000 / default` đã có admin là thành viên. `InstallationInfo.txt` trong thư mục chương trình ghi URL, DB và nguồn cho phép, không chứa mật khẩu.

Với LAN, đối chiếu dấu vân tay chứng chỉ và để quản trị viên xác nhận tin cậy. Xuất ZIP để mỗi máy khách thiết lập một lần. Tên miền chính thức có thể dùng PFX phù hợp. Let’s Encrypt miễn phí nhưng quản trị viên phải cấp, gia hạn và nhập lại; không dùng bỏ qua cảnh báo làm cấu hình lâu dài.

Chạy lại Setup để sửa cấu hình, nâng cấp hoặc cài lại với dữ liệu giữ lại. Gỡ cài đặt giữ thư mục dữ liệu. [Sao lưu và khôi phục](../README.md#backup-and-recovery-administrator-powershell) cần cùng máy, vai trò, đường dẫn và gói ứng dụng; bản sao có khóa riêng nên không công khai. DB từ xa cần sao lưu riêng. ThousanAI mặc định bật với khóa riêng từng máy, không kèm API Key mô hình; hỏi trên đám mây cần mạng và đồng ý quyền riêng tư.

## Bahasa Indonesia

Memerlukan Windows 11 x64 24H2 atau lebih baru, persetujuan administrator, dan ruang kosong minimal 5 GiB. Pembaruan memerlukan ruang tambahan untuk data dan aplikasi lama. Unduh hanya Setup EXE dan periksa SHA-256. Rilis ini belum ditandatangani; Windows dapat menampilkan penerbit tidak dikenal.

Pilih instalasi lengkap, hanya basis data, atau hanya Web. Web-only memerlukan berkas koneksi terlindungi dari host DB. Setup tidak memasang Odoo Server; konektor untuk Odoo 19 lokal yang sudah ada. Pilih IP lokal dan sumber yang diizinkan. `LocalSubnet` atau IPv4 CIDR membatasi klien pada semua profil jaringan Windows. Pengujian memerlukan sekitar 5–10 menit; ikuti langkah dan waktu tunggu yang ditampilkan.

Buka Web melalui desktop atau Start. Akun baru `admin / distributiongo`; segera ganti kata sandi. Gudang `0000 / default` sudah memiliki admin sebagai anggota. `InstallationInfo.txt` di folder program menyimpan URL, DB dan sumber yang diizinkan tanpa kata sandi.

Untuk HTTPS LAN, cocokkan sidik jari sertifikat dan setujui kepercayaan sebagai administrator. Ekspor ZIP untuk pengaturan sekali pada setiap komputer lain. Domain resmi dapat memakai PFX yang sesuai. Let’s Encrypt gratis, tetapi penerbitan, pembaruan dan impor ulang dilakukan administrator. Jangan mengandalkan melewati peringatan browser.

Jalankan Setup untuk mengubah pengaturan, memperbarui, atau memasang ulang dengan data tersimpan. Penghapusan program mempertahankan data. [Pencadangan dan pemulihan](../README.md#backup-and-recovery-administrator-powershell) memerlukan host, peran, jalur dan paket aplikasi yang sama. Cadangan berisi kunci privat; jangan publikasikan. DB jarak jauh dicadangkan terpisah. ThousanAI aktif dengan kunci unik per host tanpa API Key model; pertanyaan cloud memerlukan jaringan dan persetujuan privasi.

## 한국어

Windows 11 x64 24H2 이상, 관리자 승인 및 최소 5 GiB 여유 공간이 필요합니다. 업그레이드에는 데이터와 이전 프로그램을 보관할 추가 공간이 필요합니다. Setup EXE만 다운로드하고 SHA-256을 확인하세요. 서명되지 않은 릴리스이므로 Windows에 알 수 없는 게시자 경고가 표시될 수 있습니다.

전체, 데이터베이스 전용 또는 Web 전용을 선택하세요. Web-only는 DB 호스트의 보호된 연결 파일이 필요합니다. Odoo Server는 설치하지 않으며 커넥터는 기존 로컬 Odoo 19용입니다. 로컬 IP와 허용 원본을 선택하세요. `LocalSubnet` 또는 IPv4 CIDR 제한은 모든 Windows 네트워크 프로필에 적용됩니다. 테스트 설치 시간은 약 5~10분이며 단계와 경과 시간을 확인할 수 있습니다.

바탕 화면이나 시작 메뉴에서 Web을 여세요. 새 계정은 `admin / distributiongo`이며 암호를 변경하세요. 기본 창고 `0000 / default`에 admin이 포함됩니다. 프로그램 폴더의 `InstallationInfo.txt`에는 URL, DB 및 허용 원본이 기록되며 암호는 없습니다.

LAN HTTPS는 인증서 지문을 확인하고 관리자가 명시적으로 신뢰를 승인해야 합니다. 다른 PC는 ZIP을 내보내 한 번씩 설정하세요. 정식 도메인은 일치하는 PFX를 사용할 수 있습니다. Let’s Encrypt는 무료지만 발급, 갱신 및 재가져오기는 관리자 작업입니다. 브라우저 경고 무시를 정상 설정으로 사용하지 마세요.

Setup을 다시 실행해 설정 변경, 업그레이드 또는 보존된 데이터로 재설치할 수 있습니다. 제거 시 데이터는 유지됩니다. [백업 및 복구](../README.md#backup-and-recovery-administrator-powershell)는 동일한 호스트, 역할, 경로와 앱 패키지에서 사용합니다. 개인 키를 포함하므로 공개하지 마세요. 원격 DB는 별도 백업이 필요합니다. ThousanAI는 호스트별 키로 기본 활성화되며 모델 API 키는 포함하지 않습니다. 클라우드 질문에는 네트워크와 개인정보 동의가 필요합니다.

## Español

Requiere Windows 11 x64 24H2 o posterior, aprobación de administrador y al menos 5 GiB libres. Las actualizaciones necesitan espacio adicional para datos y programas anteriores. Descargue solo Setup EXE y compruebe SHA-256. Esta versión no está firmada; Windows puede mostrar un editor desconocido.

Elija instalación completa, solo base de datos o solo Web. Web-only requiere el archivo de conexión protegido del servidor DB. No se instala Odoo Server; el conector es para Odoo 19 local existente. Seleccione IP local y origen permitido. `LocalSubnet` o un CIDR IPv4 limita clientes en todos los perfiles de red de Windows. Las pruebas tardaron unos 5–10 minutos; consulte los pasos y el tiempo transcurrido.

Abra Web desde el escritorio o Inicio. Cuenta inicial: `admin / distributiongo`; cambie la contraseña. El almacén `0000 / default` incluye a admin. `InstallationInfo.txt` en la carpeta del programa guarda URL, DB y orígenes permitidos sin contraseñas.

Para HTTPS en LAN, verifique la huella del certificado y apruebe explícitamente la confianza como administrador. Exporte ZIP para configurar una vez cada otro equipo. Un dominio formal puede usar un PFX coincidente. Let’s Encrypt es gratuito, pero el administrador gestiona emisión, renovación e importación. No use omitir advertencias como configuración permanente.

Ejecute Setup para modificar, actualizar o reinstalar con datos conservados. La desinstalación conserva la carpeta de datos. [Copia y restauración](../README.md#backup-and-recovery-administrator-powershell) requieren el mismo equipo, rol, rutas y paquete de aplicación. Las copias contienen claves privadas: no las publique. La DB remota se copia por separado. ThousanAI se activa con una clave única por equipo, sin API Key de modelo; las preguntas en la nube requieren red y consentimiento de privacidad.

## Release validation scope / 驗收範圍

The release gate covers settings maintenance, upgrade, uninstall with retained data,
reattachment and same-host backup/restore, plus final-package integration. Existing
language and role evidence is retained. The remaining two-machine DB/Web matrix,
external Odoo and cross-computer certificate-trust acceptance are deferred; this
release does not claim those pending scenarios passed.

本輪依核定範圍驗收修改設定、升級、移除保留資料、接回、同機備份還原與最終包整合；既有語系與角色證據保留。剩餘兩機分機、外部 Odoo 及跨電腦憑證信任驗收暫緩，未宣稱通過。
