using System;
using System.Windows.Forms;
using System.Net;
using System.Net.NetworkInformation;

namespace MyWindowsApp
{
    public partial class Form1 : Form
    {
        int i;

        public Form1()
        {
            InitializeComponent();
        }

        private void button1_Click(object sender, EventArgs e)
        {
            if (timer1.Enabled)
            {
                timer1.Stop();
                label1.Text = "Press Start/Stop";
            }
            else
            {
                timer1.Start();
                label1.Text = "Timer Started";
            }
        }

        private void timer1_Tick(object sender, EventArgs e)
        {
            i++;
            richTextBox1.AppendText($"Timer ticked: {i}\n");
        }
    }
}
