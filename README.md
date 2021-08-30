# ageguessinggame
# microsoft visiul studio 2019

using System;

using System.Collections.Generic;

using System.ComponentModel;

using System.Data;

using System.Drawing;

using System.Linq;

using System.Text;

using System.Threading.Tasks;

using System.Windows.Forms;

namespace yastahmin
{
    public partial class Form1 : Form
    {
        public Form1()
        {
            InitializeComponent();
        }

        public int fvsayi;
        public int dogumyili;
        public int dogyan;

        private void button1_Click(object sender, EventArgs e)
        {
            try
            {
                fvsayi = Convert.ToInt32(fvrsayi.Text);
                dogumyili = Convert.ToInt32(dogumyıl.Text);
                if (dogumyıl.Text.Length < 4)
                {
                    MessageBox.Show("Please enter a 4 digit number");
                }
                else
                {
                if (yesdogum.Checked == true)
                {
                    dogyan = 1770;
                }
                else if (nodogum.Checked == true)
                {
                    dogyan = 1769;
                }
                int sonuc = (fvsayi * 2 + 5) * 50;
                int sonuc_2 = (sonuc + dogyan) - dogumyili;
                int sonuc_3 = sonuc_2 + 1;
                string cevir = Convert.ToString(sonuc_3);

                string ilkharf = cevir.Substring(0, 1);
                string ikinciharf = cevir.Substring(1, 2);

                string ilkharf_text = "The number I have in mind : " + ilkharf;
                string ikinci_text = "Senin yaşın : " + ikinciharf;

                birincilabel.Text = ilkharf_text;
                ikincilabel.Text = ikinci_text;

                birincilabel.Visible = true;
                ikincilabel.Visible = true;
                }
            }
            catch
            {
                MessageBox.Show("Please enter number only");
                birincilabel.Visible = false;
                ikincilabel.Visible = false;
            }
        }

        private void button1_Click_1(object sender, EventArgs e)
        {
            fvrsayi.Text = string.Empty;
            dogumyıl.Text = string.Empty;
        }
    }
}
