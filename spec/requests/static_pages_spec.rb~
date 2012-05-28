require 'spec_helper'

include ApplicationHelper

describe "Static pages" do

	let(:base_title) { "Ruby on Rails Tutorial Sample App" }

	subject { page }

	shared_examples_for "All Static Pages" do
		it { should have_selector 'h1', text: heading }
		it { should have_selector 'title', text: full_title(page_title) }
	end

	describe "Home page" do
		before { visit root_path }

		let(:heading) { 'Sample App' }
		let(:page_title) { '' }

		it_should_behave_like "All Static Pages"
		it { should_not have_selector 'title', text: '| Home' }

		it "should have the right links on the layout" do
			visit root_path
			click_link "About"
			page.should have_selector 'title', text: full_title('About Us')
			click_link "Help"
			page.should have_selector 'title', text: full_title('Help')
			click_link "Contact"
			page.should have_selector 'title', text: full_title('Contact')
			click_link "Home"
			click_link "Sign up now!"
			page.should have_selector 'title', text: full_title('Sign up')
		end
	end

	describe "Help page" do
		before { visit help_path }

		let(:heading) { 'Help' }
		let(:page_title) { 'Help' }
	end

	describe "About page" do
		before { visit about_path }

		let(:heading) { 'About' }
		let(:page_title) { 'About Us' }

		it_should_behave_like "All Static Pages"
		# it { should have_selector('h1',    text: 'About') }
		# it { should have_selector('title', text: full_title('About Us')) }
	end

	describe "Contact page" do
		before { visit contact_path }

		let(:heading) { 'Contact' }
		let(:page_title) { 'Contact' }

		it_should_behave_like "All Static Pages"
		# it { should have_selector('h1',    text: 'Contact') }
		# it { should have_selector('title', text: full_title('Contact')) }
	end

	# describe "Help page" do

	# 	it "should have the h1 'Help'" do
	# 		visit help_path
	# 		page.should have_selector('h1', :text => 'Help')
	# 	end

	# 	it "should have the title 'Help'" do
	# 		visit help_path
	# 		page.should have_selector('title',
	# 															:text => "#{base_title} | Help")
	# 	end
	# end

	# describe "About page" do

	# 	it "should have the h1 'About Us'" do
	# 		visit about_path
	# 		page.should have_selector('h1', :text => 'About Us')
	# 	end

	# 	it "should have the title 'About Us'" do
	# 		visit about_path
	# 		page.should have_selector('title',
	# 															:text => "#{base_title} | About Us")
	# 	end
	# end

	# describe "Contact Page" do

	# 	it "should have the h1 'Contact'" do
	# 		visit contact_path
	# 		page.should have_selector('h1', :text => 'Contact')
	# 	end

	# 	it "should have the title 'Contact'" do
	# 		visit contact_path
	# 		page.should have_selector('title',
	# 															:text => "#{base_title} | Contact")
	# 	end
	# end
end
