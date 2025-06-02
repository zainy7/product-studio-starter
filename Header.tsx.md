"use client";

import React from 'react';
import { Bell, User } from 'lucide-react';
import Image from 'next/image';
import Search from '@/components/ui/Search';

const Header = ({ title }: { title: string }) => {
    return (
        <div className="bg-white h-16 flex items-center justify-between p-4 border-b border-gray-200">
            {/* Page Title */}
            <h1 className="text-lg font-semibold">{title}</h1>

            {/* Search Bar and User Actions */}
            <div className="flex items-center space-x-4">
                <Search />
                <Bell className="h-5 w-5 text-gray-500 hover:text-gray-700 cursor-pointer" />
                <Image
                    src="https://picsum.photos/30/30" // Replace with actual user avatar
                    alt="User Avatar"
                    width={30}
                    height={30}
                    className="rounded-full cursor-pointer"
                />
            </div>
        </div>
    );
};

export default Header;
